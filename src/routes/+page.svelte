<script lang="ts">
    import '@fontsource/redressed'
    import Icon from '@iconify/svelte'

    let sentences: string[] = [
        'Người khiến em vừa gặp đã cười cuối cùng cũng chịu xuất hiện rùi nè',
        'Người yêu tương lai ơi, tớ chờ cậu hơi lâu rồi đấyy',
        'Mình cho phép cậu bước vào trái tim của mình đó',
        'Bình minh thì ở phía đông, còn bình yên là ở phía cậu đây rồii',
        'Vậy là thế giới bỗng dưng mất đi 2 người cô đơn <3',
        'Cậu nghĩ sao về cuộc tình đôi tarr <3',
        'Hoa đào không cần nở nữa vì người tôi đợi cuối cùng cũng đã xuất hiện rùi.',
        'Yêu cậu yêu cả cuộc đời, thương cậu thương cả một thời thanh xuân. Gửi thanh xuân của cậu ở Dự án nhéee',
        'Dự báo thời tiết nói hôm nay… tớ có cậuuuu',
        'Duyên phận bảo là chúng mình “Over hợp” đóoo',
        'Câu chuyện của chúng mình sẽ có cái kết đẹp như truyện cổ tích '
    ]
    let ok = false
    let rand_int = Math.floor(Math.random() * sentences.length)
    let sentence = sentences[rand_int]
    let number = 50 + Math.floor(rand_int * 5)
    function click() {
        ok = true
    }
</script>

{#if !ok}
    <p class="text-5xl font-['Redressed'] mb-5">BÓI TÌNH YÊU CÙNG BAN DỰ ÁN THANH NIÊN</p>
    <div class="w-80">
        <input type="text" placeholder="HỌ VÀ TÊN" class="m-1 rounded input" />
        <input
            placeholder="NGÀY THÁNG NĂM SINH"
            type="text"
            onfocus="(this.type='date')"
            onblur="(this.type='text')"
            class="m-1 rounded input" />
        <div class="flex justify-center">
            <Icon icon="ph:heart-light" width="100" height="100" />
        </div>
        <p class="text-2xl font-bold">BAN DỰ ÁN THANH NIÊN</p>
        <button class="m-4 btn variant-soft" on:click={click}>GỬI ĐI</button>
    </div>
{:else}
    <p class="text-4xl font-bold">ĐỘ TƯƠNG HỢP</p>
    <p class="font-bold text-9xl">{number}%</p>
    <p class="text-3xl">{sentence}</p>
    <p class="text-3xl font-bold">X-PROJECTS CÓ QUÀ CHO CẬU NÈ!</p>
    <a href="https://bit.ly/tuyenctvhsvhvtc">
        <Icon icon="noto:wrapped-gift" width="200" />
    </a>
{/if}
