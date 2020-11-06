---
Module Name: Az.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
ms.openlocfilehash: 5796a3692274db9b49ed16c00935ed1cd2d4e8f0
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "93611448"
---
# <span data-ttu-id="b0d81-101">Az DataLakeStore 模組</span><span class="sxs-lookup"><span data-stu-id="b0d81-101">Az.DataLakeStore Module</span></span>
## <span data-ttu-id="b0d81-102">說明</span><span class="sxs-lookup"><span data-stu-id="b0d81-102">Description</span></span>
<span data-ttu-id="b0d81-103">本節中的主題會將 azure Data Lake Store 的 Azure PowerShell Cmdlet 儲存至 Azure 資源管理員 (ARM) 架構中。</span><span class="sxs-lookup"><span data-stu-id="b0d81-103">The topics in this section document the Azure PowerShell cmdlets for Azure Data Lake Store in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="b0d81-104">DataLakeStore 命名空間中存在 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0d81-104">The cmdlets exist in the Microsoft.Azure.Commands.DataLakeStore namespace.</span></span> <span data-ttu-id="b0d81-105">這些 Cmdlet 只適用于 Azure Data Lake Storage Gen1 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-105">These cmdlets work only with Azure Data Lake Storage Gen1 accounts.</span></span>

## <span data-ttu-id="b0d81-106">Az DataLakeStore Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0d81-106">Az.DataLakeStore Cmdlets</span></span>
### [<span data-ttu-id="b0d81-107">附加 AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-107">Add-AzDataLakeStoreFirewallRule</span></span>](Add-AzDataLakeStoreFirewallRule.md)
<span data-ttu-id="b0d81-108">在指定的資料 Lake Store 帳戶中新增防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-108">Adds a firewall rule to the specified Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-109">附加 AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b0d81-109">Add-AzDataLakeStoreItemContent</span></span>](Add-AzDataLakeStoreItemContent.md)
<span data-ttu-id="b0d81-110">將內容新增至 Data Lake Store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="b0d81-110">Adds content to an item in a Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-111">附加 AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b0d81-111">Add-AzDataLakeStoreTrustedIdProvider</span></span>](Add-AzDataLakeStoreTrustedIdProvider.md)
<span data-ttu-id="b0d81-112">將信任的身分識別提供者新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-112">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-113">附加 AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-113">Add-AzDataLakeStoreVirtualNetworkRule</span></span>](Add-AzDataLakeStoreVirtualNetworkRule.md)
<span data-ttu-id="b0d81-114">將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-114">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-115">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="b0d81-115">Enable-AzDataLakeStoreKeyVault</span></span>](Enable-AzDataLakeStoreKeyVault.md)
<span data-ttu-id="b0d81-116">嘗試啟用使用者管理的金鑰保存庫以加密指定的資料 Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-116">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-117">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="b0d81-117">Export-AzDataLakeStoreChildItemProperty</span></span>](Export-AzDataLakeStoreChildItemProperty.md)
<span data-ttu-id="b0d81-118">從指定路徑將整個樹狀結構的 [磁片使用量] 與 [Acl)  (的內容匯出至輸出路徑</span><span class="sxs-lookup"><span data-stu-id="b0d81-118">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

### [<span data-ttu-id="b0d81-119">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-119">Export-AzDataLakeStoreItem</span></span>](Export-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-120">從 Data Lake Store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="b0d81-120">Downloads a file from Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-121">AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b0d81-121">Get-AzDataLakeStoreAccount</span></span>](Get-AzDataLakeStoreAccount.md)
<span data-ttu-id="b0d81-122">取得 Data Lake Store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0d81-122">Gets details of a Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-123">AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-123">Get-AzDataLakeStoreChildItem</span></span>](Get-AzDataLakeStoreChildItem.md)
<span data-ttu-id="b0d81-124">取得 Data Lake Store 中資料夾中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="b0d81-124">Gets the list of items in a folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-125">AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="b0d81-125">Get-AzDataLakeStoreChildItemSummary</span></span>](Get-AzDataLakeStoreChildItemSummary.md)
<span data-ttu-id="b0d81-126">取得指定路徑中所含之總大小、檔案和目錄的摘要</span><span class="sxs-lookup"><span data-stu-id="b0d81-126">Gets the summary of total size, files and directories contained in the path specified</span></span>

### [<span data-ttu-id="b0d81-127">AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-127">Get-AzDataLakeStoreFirewallRule</span></span>](Get-AzDataLakeStoreFirewallRule.md)
<span data-ttu-id="b0d81-128">取得指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-128">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b0d81-129">如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-129">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

### [<span data-ttu-id="b0d81-130">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-130">Get-AzDataLakeStoreItem</span></span>](Get-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-131">取得 Data Lake Store 中檔案或資料夾的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0d81-131">Gets the details of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-132">AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b0d81-132">Get-AzDataLakeStoreItemAclEntry</span></span>](Get-AzDataLakeStoreItemAclEntry.md)
<span data-ttu-id="b0d81-133">在 Data Lake Store 中取得檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="b0d81-133">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-134">AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b0d81-134">Get-AzDataLakeStoreItemContent</span></span>](Get-AzDataLakeStoreItemContent.md)
<span data-ttu-id="b0d81-135">取得 Data Lake Store 中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="b0d81-135">Gets the contents of a file in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-136">AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b0d81-136">Get-AzDataLakeStoreItemOwner</span></span>](Get-AzDataLakeStoreItemOwner.md)
<span data-ttu-id="b0d81-137">取得 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="b0d81-137">Gets the owner of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-138">AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b0d81-138">Get-AzDataLakeStoreItemPermission</span></span>](Get-AzDataLakeStoreItemPermission.md)
<span data-ttu-id="b0d81-139">取得 Data Lake Store 中檔案或資料夾的許可權八進位數。</span><span class="sxs-lookup"><span data-stu-id="b0d81-139">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-140">AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b0d81-140">Get-AzDataLakeStoreTrustedIdProvider</span></span>](Get-AzDataLakeStoreTrustedIdProvider.md)
<span data-ttu-id="b0d81-141">在指定的 Data Lake Store 中取得指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="b0d81-141">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="b0d81-142">如果沒有指定提供者，則會列出該帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="b0d81-142">If no provider is specified, then lists all providers for the account.</span></span>

### [<span data-ttu-id="b0d81-143">AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-143">Get-AzDataLakeStoreVirtualNetworkRule</span></span>](Get-AzDataLakeStoreVirtualNetworkRule.md)
<span data-ttu-id="b0d81-144">取得指定資料 Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-144">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b0d81-145">如果未指定虛擬網路規則，則會列出該帳戶的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-145">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

### [<span data-ttu-id="b0d81-146">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-146">Import-AzDataLakeStoreItem</span></span>](Import-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-147">將本機檔案或目錄上傳到 Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="b0d81-147">Uploads a local file or directory to a Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-148">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-148">Join-AzDataLakeStoreItem</span></span>](Join-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-149">加入一或多個檔案，在 Data Lake Store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="b0d81-149">Joins one or more files to create one file in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-150">移動流覽 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-150">Move-AzDataLakeStoreItem</span></span>](Move-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-151">移動或重新命名 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="b0d81-151">Moves or renames a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-152">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b0d81-152">New-AzDataLakeStoreAccount</span></span>](New-AzDataLakeStoreAccount.md)
<span data-ttu-id="b0d81-153">建立新的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-153">Creates a new Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-154">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-154">New-AzDataLakeStoreItem</span></span>](New-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-155">在 Data Lake Store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="b0d81-155">Creates a new file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-156">移除-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b0d81-156">Remove-AzDataLakeStoreAccount</span></span>](Remove-AzDataLakeStoreAccount.md)
<span data-ttu-id="b0d81-157">永久刪除 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-157">Deletes a Data Lake Store account permanently.</span></span>

### [<span data-ttu-id="b0d81-158">移除-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-158">Remove-AzDataLakeStoreFirewallRule</span></span>](Remove-AzDataLakeStoreFirewallRule.md)
<span data-ttu-id="b0d81-159">移除指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-159">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-160">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-160">Remove-AzDataLakeStoreItem</span></span>](Remove-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-161">刪除 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="b0d81-161">Deletes a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-162">移除-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b0d81-162">Remove-AzDataLakeStoreItemAcl</span></span>](Remove-AzDataLakeStoreItemAcl.md)
<span data-ttu-id="b0d81-163">清除 Data Lake Store 中的檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="b0d81-163">Clears the ACL of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-164">移除-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b0d81-164">Remove-AzDataLakeStoreItemAclEntry</span></span>](Remove-AzDataLakeStoreItemAclEntry.md)
<span data-ttu-id="b0d81-165">從 Data Lake Store 中的檔案或資料夾 ACL 中移除專案。</span><span class="sxs-lookup"><span data-stu-id="b0d81-165">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-166">移除-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b0d81-166">Remove-AzDataLakeStoreTrustedIdProvider</span></span>](Remove-AzDataLakeStoreTrustedIdProvider.md)
<span data-ttu-id="b0d81-167">移除指定資料 Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="b0d81-167">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-168">移除-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-168">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>](Remove-AzDataLakeStoreVirtualNetworkRule.md)
<span data-ttu-id="b0d81-169">移除指定資料 Lake Store 中指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-169">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-170">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b0d81-170">Set-AzDataLakeStoreAccount</span></span>](Set-AzDataLakeStoreAccount.md)
<span data-ttu-id="b0d81-171">修改 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b0d81-171">Modifies a Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-172">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-172">Set-AzDataLakeStoreFirewallRule</span></span>](Set-AzDataLakeStoreFirewallRule.md)
<span data-ttu-id="b0d81-173">修改指定資料 Lake Store 中的指定防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-173">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-174">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b0d81-174">Set-AzDataLakeStoreItemAcl</span></span>](Set-AzDataLakeStoreItemAcl.md)
<span data-ttu-id="b0d81-175">修改 Data Lake Store 中檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="b0d81-175">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-176">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b0d81-176">Set-AzDataLakeStoreItemAclEntry</span></span>](Set-AzDataLakeStoreItemAclEntry.md)
<span data-ttu-id="b0d81-177">修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="b0d81-177">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-178">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="b0d81-178">Set-AzDataLakeStoreItemExpiry</span></span>](Set-AzDataLakeStoreItemExpiry.md)
<span data-ttu-id="b0d81-179">針對 Azure Data Lake Store 帳戶中的檔案設定或移除到期時間。</span><span class="sxs-lookup"><span data-stu-id="b0d81-179">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-180">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b0d81-180">Set-AzDataLakeStoreItemOwner</span></span>](Set-AzDataLakeStoreItemOwner.md)
<span data-ttu-id="b0d81-181">修改 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="b0d81-181">Modifies the owner of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-182">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b0d81-182">Set-AzDataLakeStoreItemPermission</span></span>](Set-AzDataLakeStoreItemPermission.md)
<span data-ttu-id="b0d81-183">修改 Data Lake Store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="b0d81-183">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-184">Set-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="b0d81-184">Set-AzDataLakeStoreTrustedIdProvider</span></span>](Set-AzDataLakeStoreTrustedIdProvider.md)
<span data-ttu-id="b0d81-185">在指定的 Data Lake Store 中修改指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="b0d81-185">Modifies the specified trusted identity provider in the specified Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-186">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0d81-186">Set-AzDataLakeStoreVirtualNetworkRule</span></span>](Set-AzDataLakeStoreVirtualNetworkRule.md)
<span data-ttu-id="b0d81-187">在指定的 Data Lake Store 中修改指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b0d81-187">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

### [<span data-ttu-id="b0d81-188">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b0d81-188">Test-AzDataLakeStoreAccount</span></span>](Test-AzDataLakeStoreAccount.md)
<span data-ttu-id="b0d81-189">測試資料 Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="b0d81-189">Tests the existence of a Data Lake Store account.</span></span>

### [<span data-ttu-id="b0d81-190">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b0d81-190">Test-AzDataLakeStoreItem</span></span>](Test-AzDataLakeStoreItem.md)
<span data-ttu-id="b0d81-191">測試 Data Lake Store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="b0d81-191">Tests the existence of a file or folder in Data Lake Store.</span></span>

