---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284696"
---
# <span data-ttu-id="e73c9-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="e73c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e73c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e73c9-103">備份受管理的 HSM 中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e73c9-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="e73c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e73c9-104">SYNTAX</span></span>

### <span data-ttu-id="e73c9-105">ByKeyName (預設) </span><span class="sxs-lookup"><span data-stu-id="e73c9-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e73c9-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e73c9-107">說明</span><span class="sxs-lookup"><span data-stu-id="e73c9-107">DESCRIPTION</span></span>
<span data-ttu-id="e73c9-108">**AzManagedHsmKey** Cmdlet 會將指定的金鑰下載並儲存在檔案中，以備份受管理 HSM 中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e73c9-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="e73c9-109">如果有多個版本的金鑰，所有版本都包含在備份中。</span><span class="sxs-lookup"><span data-stu-id="e73c9-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="e73c9-110">因為下載的內容是經過加密的，所以無法在 Azure Managed HSM 之外使用。</span><span class="sxs-lookup"><span data-stu-id="e73c9-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="e73c9-111">您可以將備份的金鑰還原到其備份之訂閱中的任何受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="e73c9-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="e73c9-112">使用此 Cmdlet 的常見原因如下：</span><span class="sxs-lookup"><span data-stu-id="e73c9-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="e73c9-113">您想要保管金鑰複本，以便您在受管理的 HSM 中不小心刪除金鑰時擁有離線複本。</span><span class="sxs-lookup"><span data-stu-id="e73c9-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="e73c9-114">您使用受管理的 HSM 建立了金鑰，現在想要將該金鑰克隆至不同的 Azure 區域，這樣您就可以從分散式應用程式的所有實例中使用它。</span><span class="sxs-lookup"><span data-stu-id="e73c9-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="e73c9-115">使用 **AzManagedHsmKey** Cmdlet 以加密格式來檢索金鑰，然後使用 Restore-AzManagedHsmKey Cmdlet，並在第二個區域中指定受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="e73c9-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="e73c9-116">示例</span><span class="sxs-lookup"><span data-stu-id="e73c9-116">EXAMPLES</span></span>

### <span data-ttu-id="e73c9-117">範例1：使用自動產生的檔案名備份金鑰</span><span class="sxs-lookup"><span data-stu-id="e73c9-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="e73c9-118">這個命令會從受管理的 HSM （名為 testmhsm）中檢索名為 testkey 的索引鍵，並將該金鑰的備份儲存到自動為您命名的檔案，並顯示檔案名。</span><span class="sxs-lookup"><span data-stu-id="e73c9-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="e73c9-119">參數</span><span class="sxs-lookup"><span data-stu-id="e73c9-119">PARAMETERS</span></span>

### <span data-ttu-id="e73c9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73c9-120">-DefaultProfile</span></span>
<span data-ttu-id="e73c9-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e73c9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e73c9-122">-Force</span></span>
<span data-ttu-id="e73c9-123">覆寫指定的檔案（如果有的話）</span><span class="sxs-lookup"><span data-stu-id="e73c9-123">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e73c9-124">-HsmName</span></span>
<span data-ttu-id="e73c9-125">HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="e73c9-125">HSM name.</span></span> <span data-ttu-id="e73c9-126">Cmdlet 根據名稱和目前所選的環境來構造受管理的 HSM 的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e73c9-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e73c9-127">-InputObject</span></span>
<span data-ttu-id="e73c9-128">要備份的主要捆綁，從檢索呼叫的輸出中流水線。</span><span class="sxs-lookup"><span data-stu-id="e73c9-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="e73c9-129">-Name</span></span>
<span data-ttu-id="e73c9-130">索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="e73c9-130">Key name.</span></span>
<span data-ttu-id="e73c9-131">Cmdlet 會從 managed HSM 名稱、目前已選取的環境和金鑰名稱來構造金鑰的 FQDN。</span><span class="sxs-lookup"><span data-stu-id="e73c9-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e73c9-132">-OutputFile</span></span>
<span data-ttu-id="e73c9-133">輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="e73c9-133">Output file.</span></span>
<span data-ttu-id="e73c9-134">儲存已備份之金鑰 blob 的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="e73c9-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="e73c9-135">如果不存在，則會選取預設的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e73c9-135">If not present, a default filename is chosen.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-136">-確認</span><span class="sxs-lookup"><span data-stu-id="e73c9-136">-Confirm</span></span>
<span data-ttu-id="e73c9-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e73c9-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73c9-138">-WhatIf</span></span>
<span data-ttu-id="e73c9-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e73c9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73c9-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e73c9-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73c9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73c9-141">CommonParameters</span></span>
<span data-ttu-id="e73c9-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e73c9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73c9-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e73c9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73c9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e73c9-144">INPUTS</span></span>

### <span data-ttu-id="e73c9-145">PSKeyVaultKeyIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e73c9-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="e73c9-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e73c9-146">OUTPUTS</span></span>

### <span data-ttu-id="e73c9-147">System.object</span><span class="sxs-lookup"><span data-stu-id="e73c9-147">System.String</span></span>

## <span data-ttu-id="e73c9-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e73c9-148">NOTES</span></span>

## <span data-ttu-id="e73c9-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e73c9-149">RELATED LINKS</span></span>

[<span data-ttu-id="e73c9-150">附加 AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="e73c9-151">AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="e73c9-152">移除-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="e73c9-153">復原-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="e73c9-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="e73c9-154">更新-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="e73c9-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e73c9-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)