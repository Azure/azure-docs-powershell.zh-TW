---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskUpdateConfig.md
ms.openlocfilehash: d50a00ef6c68958f24fbf498adac20691aaaa750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445100"
---
# <span data-ttu-id="0c2e6-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0c2e6-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="0c2e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2e6-103">建立可設定的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c2e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c2e6-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c2e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c2e6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c2e6-106">**新的-AzureRmDiskUpdateConfig** Cmdlet 會建立一個可設定的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="0c2e6-107">示例</span><span class="sxs-lookup"><span data-stu-id="0c2e6-107">EXAMPLES</span></span>

### <span data-ttu-id="0c2e6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0c2e6-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="0c2e6-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0c2e6-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0c2e6-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="0c2e6-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0c2e6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0c2e6-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="0c2e6-114">這個命令會將資源群組 ' ResourceGroup01 ' 中的名稱為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0c2e6-115">參數</span><span class="sxs-lookup"><span data-stu-id="0c2e6-115">PARAMETERS</span></span>

### <span data-ttu-id="0c2e6-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0c2e6-116">-CreateOption</span></span>
<span data-ttu-id="0c2e6-117">指定此 Cmdlet 是否在虛擬機器中從平臺或使用者影像建立磁片、建立空白磁片，或附加現有磁片。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-117">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2e6-118">-DefaultProfile</span></span>
<span data-ttu-id="0c2e6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0c2e6-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="0c2e6-121">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-121">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0c2e6-122">-DiskSizeGB</span></span>
<span data-ttu-id="0c2e6-123">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0c2e6-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0c2e6-125">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-125">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-126">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="0c2e6-126">-ImageReference</span></span>
<span data-ttu-id="0c2e6-127">指定磁片上的影像參照。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-127">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-128">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0c2e6-128">-KeyEncryptionKey</span></span>
<span data-ttu-id="0c2e6-129">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-129">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="0c2e6-130">-OsType</span></span>
<span data-ttu-id="0c2e6-131">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-131">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0c2e6-132">-SkuName</span></span>
<span data-ttu-id="0c2e6-133">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0c2e6-134">-SourceResourceId</span></span>
<span data-ttu-id="0c2e6-135">指定來源資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-135">Specifies the source resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="0c2e6-136">-SourceUri</span></span>
<span data-ttu-id="0c2e6-137">指定來源 Uri。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-137">Specifies the source Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0c2e6-138">-StorageAccountId</span></span>
<span data-ttu-id="0c2e6-139">指定儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-139">Specifies the storage account ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c2e6-140">-Tag</span></span>
<span data-ttu-id="0c2e6-141">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c2e6-142">-確認</span><span class="sxs-lookup"><span data-stu-id="0c2e6-142">-Confirm</span></span>
<span data-ttu-id="0c2e6-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2e6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2e6-144">-WhatIf</span></span>
<span data-ttu-id="0c2e6-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c2e6-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2e6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2e6-147">CommonParameters</span></span>
<span data-ttu-id="0c2e6-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2e6-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c2e6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2e6-150">輸入</span><span class="sxs-lookup"><span data-stu-id="0c2e6-150">INPUTS</span></span>

### <span data-ttu-id="0c2e6-151">"StorageAccountTypes" 1 [[14.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="0c2e6-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="0c2e6-152">系統. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [System. Int32，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]] system. 集合. Hashtable = `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]，區域性 = 中立，PublicKeyToken =]]，</span><span class="sxs-lookup"><span data-stu-id="0c2e6-152">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="0c2e6-153">輸出</span><span class="sxs-lookup"><span data-stu-id="0c2e6-153">OUTPUTS</span></span>

### <span data-ttu-id="0c2e6-154">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="0c2e6-154">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="0c2e6-155">筆記</span><span class="sxs-lookup"><span data-stu-id="0c2e6-155">NOTES</span></span>

## <span data-ttu-id="0c2e6-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c2e6-156">RELATED LINKS</span></span>

