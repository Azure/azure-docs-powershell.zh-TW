---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: d1cf3757596a56336c25c46bd6c4e38687888d6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143006"
---
# <span data-ttu-id="62977-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="62977-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="62977-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62977-102">SYNOPSIS</span></span>
<span data-ttu-id="62977-103">從備份中完整還原受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="62977-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="62977-104">句法</span><span class="sxs-lookup"><span data-stu-id="62977-104">SYNTAX</span></span>

### <span data-ttu-id="62977-105">InteractiveStorageName (預設) </span><span class="sxs-lookup"><span data-stu-id="62977-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62977-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="62977-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62977-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="62977-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62977-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="62977-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62977-109">說明</span><span class="sxs-lookup"><span data-stu-id="62977-109">DESCRIPTION</span></span>
<span data-ttu-id="62977-110">從儲存在儲存空間帳戶中的備份中完整還原受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="62977-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="62977-111">使用 [ `Backup-AzKeyVault` 備份]。</span><span class="sxs-lookup"><span data-stu-id="62977-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="62977-112">示例</span><span class="sxs-lookup"><span data-stu-id="62977-112">EXAMPLES</span></span>

### <span data-ttu-id="62977-113">範例1</span><span class="sxs-lookup"><span data-stu-id="62977-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="62977-114">這個範例會將儲存在存儲容器 "mhsm-myHsm-2020101308504935" 的資料夾（"HTTPs：//{accountName"）中的備份還原儲存在</span><span class="sxs-lookup"><span data-stu-id="62977-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="62977-115">參數</span><span class="sxs-lookup"><span data-stu-id="62977-115">PARAMETERS</span></span>

### <span data-ttu-id="62977-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="62977-116">-BackupFolder</span></span>
<span data-ttu-id="62977-117">備份的資料夾名稱，例如 ' mhsm-*-2020101309020403」。它也可以嵌套，例如「備份/mhsm-*-2020101309020403」。</span><span class="sxs-lookup"><span data-stu-id="62977-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62977-118">-DefaultProfile</span></span>
<span data-ttu-id="62977-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62977-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62977-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="62977-120">-HsmName</span></span>
<span data-ttu-id="62977-121">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="62977-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="62977-122">-HsmObject</span></span>
<span data-ttu-id="62977-123">受管理的 HSM 物件</span><span class="sxs-lookup"><span data-stu-id="62977-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62977-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="62977-124">-KeyName</span></span>
<span data-ttu-id="62977-125">要還原的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="62977-125">Key name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62977-126">-PassThru</span></span>
<span data-ttu-id="62977-127">還原 HSM 時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="62977-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="62977-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="62977-128">-SasToken</span></span>
<span data-ttu-id="62977-129">共用存取簽名 (SAS) 權杖來驗證儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="62977-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62977-130">-StorageAccountName</span></span>
<span data-ttu-id="62977-131">儲存備份的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="62977-131">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="62977-132">-StorageContainerName</span></span>
<span data-ttu-id="62977-133">要儲存備份之 blob 容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="62977-133">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="62977-134">-StorageContainerUri</span></span>
<span data-ttu-id="62977-135">儲存備份的儲存空間容器 URI。</span><span class="sxs-lookup"><span data-stu-id="62977-135">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62977-136">-確認</span><span class="sxs-lookup"><span data-stu-id="62977-136">-Confirm</span></span>
<span data-ttu-id="62977-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62977-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62977-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62977-138">-WhatIf</span></span>
<span data-ttu-id="62977-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62977-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62977-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62977-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62977-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62977-141">CommonParameters</span></span>
<span data-ttu-id="62977-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62977-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62977-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="62977-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62977-144">輸入</span><span class="sxs-lookup"><span data-stu-id="62977-144">INPUTS</span></span>

### <span data-ttu-id="62977-145">所有</span><span class="sxs-lookup"><span data-stu-id="62977-145">None</span></span>

## <span data-ttu-id="62977-146">輸出</span><span class="sxs-lookup"><span data-stu-id="62977-146">OUTPUTS</span></span>

### <span data-ttu-id="62977-147">System.object</span><span class="sxs-lookup"><span data-stu-id="62977-147">System.Boolean</span></span>

## <span data-ttu-id="62977-148">筆記</span><span class="sxs-lookup"><span data-stu-id="62977-148">NOTES</span></span>

## <span data-ttu-id="62977-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="62977-149">RELATED LINKS</span></span>
