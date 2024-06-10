<script>
    import { Footer, FooterCopyright, FooterLinkGroup, FooterLink, FooterBrand, FooterIcon } from 'flowbite-svelte';
    import Icon from '@iconify/svelte';
    import { Contact, Page, Others, Icon as icons } from '../../data/FootNav';
  </script>
  
<Footer class="dark:bg-gray-900 border-t-2 mt-12">
  <FooterCopyright class="mt-4" copyrightMessage="Made with ❤️ using Svelte" href="/" by="ilhamjaya08" />
</Footer>
  <!---<Footer footerType="socialmedia" class="border-t-2 border-gray-200 mt-4">
    <div class="md:flex md:justify-between">
      <div class="mb-6 md:mb-0">
        <FooterBrand href="/" src="https://avatars.githubusercontent.com/u/141555404?v=4" alt="Muhammad Ilham Jaya " name="ilhamjaya08" />
      </div>
      <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
        <div>
          <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Contact</h2>
          <FooterLinkGroup>
            {#each Contact as contact}
            <FooterLink liClass="mb-4" href={contact.href}>{contact.title}</FooterLink>
            {/each}
          </FooterLinkGroup>
        </div>
        <div>
          <h2 class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white">Page</h2>
          <FooterLinkGroup>
            {#each Page as page}
            <FooterLink liClass="mb-4" href={page.href}>{page.title}</FooterLink>
            {/each}
          </FooterLinkGroup>
        </div>
        <div>
          <h2 class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white">Others</h2>
          <FooterLinkGroup>
            {#each Others as others}
            <FooterLink liClass="mb-4" href={others.href}>{others.title}</FooterLink>
            {/each}
          </FooterLinkGroup>
        </div>
      </div>
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
    <div class="sm:flex sm:items-center sm:justify-between">
      <FooterCopyright href="/" by="Muhammad Ilham Jaya " />
      <div class="flex mt-4 space-x-6 rtl:space-x-reverse sm:justify-center sm:mt-0">
        {#each icons as icon}
        <FooterIcon href={icon.href}>
          <Icon icon={icon.icon} class="w-5 h-5 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
        </FooterIcon>
        {/each}
      </div>
    </div>
  </Footer>-->