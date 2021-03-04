---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 36dfd9e5b4e1ddddadb745b2c44ab65b97833baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908537"
---
# <span data-ttu-id="6422c-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6422c-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="6422c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6422c-102">SYNOPSIS</span></span>
<span data-ttu-id="6422c-103">從備份完全還原受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="6422c-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="6422c-104">語法</span><span class="sxs-lookup"><span data-stu-id="6422c-104">SYNTAX</span></span>

### <span data-ttu-id="6422c-105">InteractiveStorageName (預設) </span><span class="sxs-lookup"><span data-stu-id="6422c-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6422c-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="6422c-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] [-HsmName] <String>
 -StorageContainerUri <Uri> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6422c-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="6422c-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageContainerUri <Uri>
 -SasToken <SecureString> -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6422c-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="6422c-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-KeyName <String>] [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6422c-109">描述</span><span class="sxs-lookup"><span data-stu-id="6422c-109">DESCRIPTION</span></span>
<span data-ttu-id="6422c-110">從儲存帳戶中儲存的備份完全還原受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="6422c-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="6422c-111">用於 `Backup-AzKeyVault` 備份。</span><span class="sxs-lookup"><span data-stu-id="6422c-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="6422c-112">例子</span><span class="sxs-lookup"><span data-stu-id="6422c-112">EXAMPLES</span></span>

### <span data-ttu-id="6422c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="6422c-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="6422c-114">此範例會還原儲存在儲存容器 "HTTPs：//{accountName}.blob.core.windows.net/{containerName}" 資料夾中的備份，該資料夾名為 "mhtm-myHtm-2020101308504935"。</span><span class="sxs-lookup"><span data-stu-id="6422c-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="6422c-115">參數</span><span class="sxs-lookup"><span data-stu-id="6422c-115">PARAMETERS</span></span>

### <span data-ttu-id="6422c-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="6422c-116">-BackupFolder</span></span>
<span data-ttu-id="6422c-117">備份的資料夾名稱，例如'm進m-*-2020101309020403'。它也可以以巢巢式表示，例如'backups/m-*-2020101309020403'。</span><span class="sxs-lookup"><span data-stu-id="6422c-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

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

### <span data-ttu-id="6422c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6422c-118">-DefaultProfile</span></span>
<span data-ttu-id="6422c-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6422c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6422c-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6422c-120">-HsmName</span></span>
<span data-ttu-id="6422c-121">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="6422c-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="6422c-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="6422c-122">-HsmObject</span></span>
<span data-ttu-id="6422c-123">Managed HSM 物件</span><span class="sxs-lookup"><span data-stu-id="6422c-123">Managed HSM object</span></span>

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

### <span data-ttu-id="6422c-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="6422c-124">-KeyName</span></span>
<span data-ttu-id="6422c-125">要還原的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="6422c-125">Key name to restore.</span></span>

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

### <span data-ttu-id="6422c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6422c-126">-PassThru</span></span>
<span data-ttu-id="6422c-127">還原 HSM 時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="6422c-127">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="6422c-128">-SasToken</span><span class="sxs-lookup"><span data-stu-id="6422c-128">-SasToken</span></span>
<span data-ttu-id="6422c-129">共用存取簽章 (SAS) 權杖，以驗證儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="6422c-129">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="6422c-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6422c-130">-StorageAccountName</span></span>
<span data-ttu-id="6422c-131">儲存備份的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6422c-131">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="6422c-132">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="6422c-132">-StorageContainerName</span></span>
<span data-ttu-id="6422c-133">要儲存備份的 Blob 容器名稱。</span><span class="sxs-lookup"><span data-stu-id="6422c-133">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="6422c-134">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="6422c-134">-StorageContainerUri</span></span>
<span data-ttu-id="6422c-135">儲存備份的儲存容器 URI。</span><span class="sxs-lookup"><span data-stu-id="6422c-135">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="6422c-136">-確認</span><span class="sxs-lookup"><span data-stu-id="6422c-136">-Confirm</span></span>
<span data-ttu-id="6422c-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6422c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6422c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6422c-138">-WhatIf</span></span>
<span data-ttu-id="6422c-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6422c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6422c-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6422c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6422c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6422c-141">CommonParameters</span></span>
<span data-ttu-id="6422c-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6422c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6422c-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6422c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6422c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="6422c-144">INPUTS</span></span>

### <span data-ttu-id="6422c-145">沒有</span><span class="sxs-lookup"><span data-stu-id="6422c-145">None</span></span>

## <span data-ttu-id="6422c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="6422c-146">OUTPUTS</span></span>

### <span data-ttu-id="6422c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6422c-147">System.Boolean</span></span>

## <span data-ttu-id="6422c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="6422c-148">NOTES</span></span>

## <span data-ttu-id="6422c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="6422c-149">RELATED LINKS</span></span>
