---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 9f1d18586d0d903f705b3b2be21dd8f864efcf9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910486"
---
# <span data-ttu-id="f1a59-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f1a59-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="f1a59-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1a59-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a59-103">完整備份受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="f1a59-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="f1a59-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1a59-104">SYNTAX</span></span>

### <span data-ttu-id="f1a59-105">InteractiveStorageName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1a59-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a59-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="f1a59-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a59-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="f1a59-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a59-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="f1a59-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a59-109">描述</span><span class="sxs-lookup"><span data-stu-id="f1a59-109">DESCRIPTION</span></span>
<span data-ttu-id="f1a59-110">將受管理的 HSM 完整備份到儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f1a59-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="f1a59-111">用於 `Restore-AzKeyVault` 還原備份。</span><span class="sxs-lookup"><span data-stu-id="f1a59-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="f1a59-112">例子</span><span class="sxs-lookup"><span data-stu-id="f1a59-112">EXAMPLES</span></span>

### <span data-ttu-id="f1a59-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f1a59-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="f1a59-114">Cmdlet 會建立一個資料夾 (在儲存) 容器中，將備份儲存在該資料夾中，然後 `mhsm-{name}-{timestamp}` 輸出檔案夾 URI。</span><span class="sxs-lookup"><span data-stu-id="f1a59-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="f1a59-115">參數</span><span class="sxs-lookup"><span data-stu-id="f1a59-115">PARAMETERS</span></span>

### <span data-ttu-id="f1a59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a59-116">-DefaultProfile</span></span>
<span data-ttu-id="f1a59-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1a59-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a59-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f1a59-118">-HsmName</span></span>
<span data-ttu-id="f1a59-119">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1a59-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="f1a59-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="f1a59-120">-HsmObject</span></span>
<span data-ttu-id="f1a59-121">Managed HSM 物件</span><span class="sxs-lookup"><span data-stu-id="f1a59-121">Managed HSM object</span></span>

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

### <span data-ttu-id="f1a59-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="f1a59-122">-SasToken</span></span>
<span data-ttu-id="f1a59-123">共用存取簽章 (SAS) 權杖，以驗證儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="f1a59-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="f1a59-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1a59-124">-StorageAccountName</span></span>
<span data-ttu-id="f1a59-125">儲存備份的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f1a59-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="f1a59-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f1a59-126">-StorageContainerName</span></span>
<span data-ttu-id="f1a59-127">要儲存備份的 Blob 容器名稱。</span><span class="sxs-lookup"><span data-stu-id="f1a59-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="f1a59-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="f1a59-128">-StorageContainerUri</span></span>
<span data-ttu-id="f1a59-129">儲存備份的儲存容器 URI。</span><span class="sxs-lookup"><span data-stu-id="f1a59-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="f1a59-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f1a59-130">-Confirm</span></span>
<span data-ttu-id="f1a59-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1a59-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a59-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a59-132">-WhatIf</span></span>
<span data-ttu-id="f1a59-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1a59-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a59-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1a59-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a59-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a59-135">CommonParameters</span></span>
<span data-ttu-id="f1a59-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1a59-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a59-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1a59-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a59-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f1a59-138">INPUTS</span></span>

### <span data-ttu-id="f1a59-139">沒有</span><span class="sxs-lookup"><span data-stu-id="f1a59-139">None</span></span>

## <span data-ttu-id="f1a59-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f1a59-140">OUTPUTS</span></span>

### <span data-ttu-id="f1a59-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a59-141">System.String</span></span>

## <span data-ttu-id="f1a59-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f1a59-142">NOTES</span></span>

## <span data-ttu-id="f1a59-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1a59-143">RELATED LINKS</span></span>
