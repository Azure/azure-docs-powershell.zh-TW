---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801797"
---
# <span data-ttu-id="3edc6-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="3edc6-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="3edc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3edc6-102">SYNOPSIS</span></span>
<span data-ttu-id="3edc6-103">建立可設定的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="3edc6-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3edc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="3edc6-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3edc6-105">說明</span><span class="sxs-lookup"><span data-stu-id="3edc6-105">DESCRIPTION</span></span>
<span data-ttu-id="3edc6-106">**新的-AzureRmDiskUpdateConfig** Cmdlet 會建立一個可設定的磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="3edc6-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="3edc6-107">示例</span><span class="sxs-lookup"><span data-stu-id="3edc6-107">EXAMPLES</span></span>

### <span data-ttu-id="3edc6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3edc6-108">Example 1</span></span>
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

<span data-ttu-id="3edc6-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="3edc6-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="3edc6-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="3edc6-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="3edc6-111">第二個和第三個命令會設定磁片更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="3edc6-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="3edc6-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="3edc6-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="3edc6-113">範例2</span><span class="sxs-lookup"><span data-stu-id="3edc6-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="3edc6-114">這個命令會將資源群組 ' ResourceGroup01 ' 中的名稱為 ' Disk01 ' 的現有磁片更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="3edc6-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="3edc6-115">參數</span><span class="sxs-lookup"><span data-stu-id="3edc6-115">PARAMETERS</span></span>

### <span data-ttu-id="3edc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3edc6-116">-DefaultProfile</span></span>
<span data-ttu-id="3edc6-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3edc6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3edc6-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="3edc6-119">指定磁片上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="3edc6-119">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3edc6-120">-DiskSizeGB</span></span>
<span data-ttu-id="3edc6-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="3edc6-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="3edc6-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="3edc6-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="3edc6-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3edc6-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="3edc6-125">指定磁片上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="3edc6-125">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="3edc6-126">-OsType</span></span>
<span data-ttu-id="3edc6-127">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="3edc6-127">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3edc6-128">-SkuName</span></span>
<span data-ttu-id="3edc6-129">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="3edc6-129">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="3edc6-130">-Tag</span></span>
<span data-ttu-id="3edc6-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3edc6-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3edc6-132">例如：</span><span class="sxs-lookup"><span data-stu-id="3edc6-132">For example:</span></span>

<span data-ttu-id="3edc6-133">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3edc6-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="3edc6-134">-Confirm</span></span>
<span data-ttu-id="3edc6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3edc6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3edc6-136">-WhatIf</span></span>
<span data-ttu-id="3edc6-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3edc6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3edc6-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3edc6-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3edc6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3edc6-139">CommonParameters</span></span>
<span data-ttu-id="3edc6-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3edc6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3edc6-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3edc6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3edc6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3edc6-142">INPUTS</span></span>

### <span data-ttu-id="3edc6-143">所有</span><span class="sxs-lookup"><span data-stu-id="3edc6-143">None</span></span>
<span data-ttu-id="3edc6-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3edc6-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3edc6-145">輸出</span><span class="sxs-lookup"><span data-stu-id="3edc6-145">OUTPUTS</span></span>

### <span data-ttu-id="3edc6-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="3edc6-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="3edc6-147">筆記</span><span class="sxs-lookup"><span data-stu-id="3edc6-147">NOTES</span></span>

## <span data-ttu-id="3edc6-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="3edc6-148">RELATED LINKS</span></span>

