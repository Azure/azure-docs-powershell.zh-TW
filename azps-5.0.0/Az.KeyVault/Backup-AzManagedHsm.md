---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136766"
---
# <span data-ttu-id="f8cc1-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f8cc1-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="f8cc1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cc1-103">完整備份受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="f8cc1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8cc1-104">SYNTAX</span></span>

### <span data-ttu-id="f8cc1-105">InteractiveStorageName (預設) </span><span class="sxs-lookup"><span data-stu-id="f8cc1-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cc1-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="f8cc1-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cc1-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="f8cc1-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cc1-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="f8cc1-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8cc1-109">說明</span><span class="sxs-lookup"><span data-stu-id="f8cc1-109">DESCRIPTION</span></span>
<span data-ttu-id="f8cc1-110">將受管理的 HSM 完整備份至儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="f8cc1-111">用 `Restore-AzManagedHsm` 來還原備份。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="f8cc1-112">示例</span><span class="sxs-lookup"><span data-stu-id="f8cc1-112">EXAMPLES</span></span>

### <span data-ttu-id="f8cc1-113">範例1</span><span class="sxs-lookup"><span data-stu-id="f8cc1-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="f8cc1-114">這個 Cmdlet 會在 storage 容器中建立 (通常稱為) 的資料夾 `mhsm-{name}-{timestamp}` ，並將備份儲存在該資料夾中，並輸出檔案夾 URI。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="f8cc1-115">參數</span><span class="sxs-lookup"><span data-stu-id="f8cc1-115">PARAMETERS</span></span>

### <span data-ttu-id="f8cc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cc1-116">-DefaultProfile</span></span>
<span data-ttu-id="f8cc1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8cc1-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="f8cc1-118">-HsmObject</span></span>
<span data-ttu-id="f8cc1-119">受管理的 HSM 物件</span><span class="sxs-lookup"><span data-stu-id="f8cc1-119">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8cc1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8cc1-120">-Name</span></span>
<span data-ttu-id="f8cc1-121">HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8cc1-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="f8cc1-122">-SasToken</span></span>
<span data-ttu-id="f8cc1-123">共用存取簽名 (SAS) 權杖來驗證儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="f8cc1-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8cc1-124">-StorageAccountName</span></span>
<span data-ttu-id="f8cc1-125">儲存備份的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="f8cc1-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="f8cc1-126">-StorageContainerName</span></span>
<span data-ttu-id="f8cc1-127">要儲存備份之 blob 容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="f8cc1-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="f8cc1-128">-StorageContainerUri</span></span>
<span data-ttu-id="f8cc1-129">儲存備份的儲存空間容器 URI。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="f8cc1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f8cc1-130">-Confirm</span></span>
<span data-ttu-id="f8cc1-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8cc1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8cc1-132">-WhatIf</span></span>
<span data-ttu-id="f8cc1-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8cc1-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8cc1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cc1-135">CommonParameters</span></span>
<span data-ttu-id="f8cc1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cc1-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f8cc1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cc1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="f8cc1-138">INPUTS</span></span>

### <span data-ttu-id="f8cc1-139">所有</span><span class="sxs-lookup"><span data-stu-id="f8cc1-139">None</span></span>

## <span data-ttu-id="f8cc1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f8cc1-140">OUTPUTS</span></span>

### <span data-ttu-id="f8cc1-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f8cc1-141">System.String</span></span>

## <span data-ttu-id="f8cc1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f8cc1-142">NOTES</span></span>

## <span data-ttu-id="f8cc1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8cc1-143">RELATED LINKS</span></span>
