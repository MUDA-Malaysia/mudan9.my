<script lang="ts">
  const candidates = [
    {
      name: 'Danial Abdul Majeed',
      no: 'P041',
      parliament: 'Kepala Batas',
      state: 'Pulau Penang',
      image: 'images/ge15/danial-abdul-majeed.webp'
    },
    {
      name: 'Siti Rahayu Baharin (Cikgu Rahayu)',
      no: 'P095',
      parliament: 'Tanjong Karang',
      state: 'Selangor',
      image: 'images/ge15/cikgu-rahayu.webp'
    },
    {
      name: 'Mutalib Uthman',
      no: 'P134',
      parliament: 'Masjid Tanah',
      state: 'Melaka',
      image: 'images/ge15/mutalib-uthman.webp'
    },
    {
      name: 'Syed Saddiq',
      no: 'P146',
      parliament: 'Muar',
      state: 'Johor',
      image: 'images/ge15/syed-saddiq.webp'
    },
    {
      name: 'Lim Wei Jiet',
      no: 'P165',
      parliament: 'Tanjung Piai',
      state: 'Johor',
      image: 'images/ge15/lim-wei-jiet.webp'
    },
    {
      name: 'Shahrizal Denci',
      no: 'P168',
      parliament: 'Kota Marudu',
      state: 'Sabah',
      image: 'images/ge15/shahrizal-denci.webp'
    }
  ];
</script>

<ul>
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
      </span>
    </li>
  {/each}
</ul>

<style lang="scss">
  ul {
    list-style: none;
    list-style-position: inside;
    padding: 1.5rem;
    display: block;

    li {
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
      }
    }
  }
</style>
