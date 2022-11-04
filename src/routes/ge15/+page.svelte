<script lang="ts">
  const candidates = [
    {
      name: 'Danial Abdul Majeed',
      no: 'P041',
      parliament: 'Kepala Batas',
      state: 'Pulau Penang',
      image: 'images/ge15/danial-abdul-majeed.webp',
      socialMedia: {
        fb: 'https://www.facebook.com/danialabdmajeed',
        ig: 'https://www.instagram.com/danialabdmajeed/',
        twitter: 'https://twitter.com/danialabdmajeed'
      }
    },
    {
      name: 'Siti Rahayu Baharin (Cikgu Rahayu)',
      no: 'P095',
      parliament: 'Tanjong Karang',
      state: 'Selangor',
      image: 'images/ge15/cikgu-rahayu.webp',
      socialMedia: {
        fb: 'https://www.facebook.com/siti.baharin',
        ig: 'https://www.instagram.com/cikgurahayu',
        twitter: 'https://twitter.com/CikguRahayu'
      }
    },
    {
      name: 'Mutalib Uthman',
      no: 'P134',
      parliament: 'Masjid Tanah',
      state: 'Melaka',
      image: 'images/ge15/mutalib-uthman.webp',
      socialMedia: {
        fb: 'https://www.facebook.com/MudalibUthman/'
      }
    },
    {
      name: 'Syed Saddiq',
      no: 'P146',
      parliament: 'Muar',
      state: 'Johor',
      image: 'images/ge15/syed-saddiq.webp',
      socialMedia: {
        fb: 'https://www.facebook.com/syedsaddiqofficial',
        ig: 'https://www.instagram.com/syedsaddiq/',
        twitter: 'https://twitter.com/SyedSaddiq'
      }
    },
    {
      name: 'Lim Wei Jiet',
      no: 'P165',
      parliament: 'Tanjung Piai',
      state: 'Johor',
      image: 'images/ge15/lim-wei-jiet.webp',
      socialMedia: {
        fb: 'https://www.facebook.com/limweijiet91',
        ig: 'https://www.instagram.com/lim_weijiet/',
        twitter: 'https://twitter.com/lim_weijiet'
      }
    },
    {
      name: 'Shahrizal Denci',
      no: 'P168',
      parliament: 'Kota Marudu',
      state: 'Sabah',
      image: 'images/ge15/shahrizal-denci.webp',
      socialMedia: {
        fb: 'https://www.facebook.com/dencishahrizal',
        ig: 'https://www.instagram.com/shahrizaldenci/',
        twitter: 'https://twitter.com/DenciShahrizal'
      }
    }
  ];
</script>

<h1>MUDA Candidates</h1>
<ul class="candidate-list">
  {#each candidates as candidate}
    <li>
      <span class="avatar"
        ><div class="thumbnail">
          <div class="wrapper">
            <img src={candidate.image} alt={candidate.name} />
          </div>
        </div></span
      >
      <span class="info">
        <div class="no">{`${candidate.no} - ${candidate.parliament} (${candidate.state})`}</div>
        <div>{candidate.name}</div>
        {#if candidate.socialMedia}
          <ul class="social-media-list">
            {#if candidate.socialMedia.fb}
              <li>
                <a href={candidate.socialMedia.fb} target="_blank"
                  >{@html `<svg width="24px" height="24px"><use href="#facebook" /></svg>`}</a
                >
              </li>
            {/if}
            <!-- {#if candidate.socialMedia.ig}
              <li>
                <a href={candidate.socialMedia.ig} target="_blank"
                  >{@html `<svg width="24px" height="24px"><use href="#instagram" /></svg>`}</a
                >
              </li>
            {/if} -->
            {#if candidate.socialMedia.twitter}
              <li>
                <a href={candidate.socialMedia.twitter} target="_blank"
                  >{@html `<svg width="24px" height="24px"><use href="#twitter" /></svg>`}</a
                >
              </li>
            {/if}
          </ul>
        {/if}
      </span>
    </li>
  {/each}
</ul>

<style lang="scss">
  .candidate-list {
    list-style: none;
    list-style-position: inside;
    padding: 1.5rem;
    display: flex;
    flex-direction: column;

    & > li {
      display: inline-flex;
      margin-bottom: 1.5rem;

      .avatar {
        width: 40%;
      }

      .thumbnail {
        position: relative;
        width: 180px;
        max-width: 100%;
        padding-top: 100%;
        background-color: red;

        .wrapper {
          position: absolute;
          top: 0;
          left: 0;
          bottom: 0;
          right: 0;
          color: white;
        }

        img {
          display: block;
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }

      .info {
        padding-left: 15px;

        .no {
          font-weight: bold;
          font-size: 1.2rem;
        }

        .social-media-list {
          list-style: none;
          list-style-position: inside;
          display: flex;
          flex-direction: row;
          align-items: center;
          padding: 15px 0;

          & > li {
            margin-right: 10px;
          }
        }
      }
    }
  }
</style>
