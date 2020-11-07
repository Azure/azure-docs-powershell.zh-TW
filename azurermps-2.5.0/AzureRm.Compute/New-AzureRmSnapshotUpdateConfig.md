---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
ms.openlocfilehash: 033b183c763be266b29aadf47a57e760e2432452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801789"
---
# <span data-ttu-id="ac9ca-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ac9ca-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="ac9ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9ca-103">建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac9ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac9ca-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac9ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ac9ca-106">**新的-AzureRmSnapshotUpdateConfig** Cmdlet 會建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="ac9ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac9ca-107">EXAMPLES</span></span>

### <span data-ttu-id="ac9ca-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ac9ca-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="ac9ca-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ac9ca-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ac9ca-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="ac9ca-112">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ac9ca-113">範例2</span><span class="sxs-lookup"><span data-stu-id="ac9ca-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="ac9ca-114">這個命令會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ac9ca-115">參數</span><span class="sxs-lookup"><span data-stu-id="ac9ca-115">PARAMETERS</span></span>

### <span data-ttu-id="ac9ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9ca-116">-DefaultProfile</span></span>
<span data-ttu-id="ac9ca-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac9ca-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ac9ca-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ac9ca-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="ac9ca-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ac9ca-120">-DiskSizeGB</span></span>
<span data-ttu-id="ac9ca-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ac9ca-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ac9ca-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ac9ca-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ac9ca-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ac9ca-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="ac9ca-125">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="ac9ca-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="ac9ca-126">-OsType</span></span>
<span data-ttu-id="ac9ca-127">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ac9ca-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ac9ca-128">-SkuName</span></span>
<span data-ttu-id="ac9ca-129">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ac9ca-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac9ca-130">-Tag</span></span>
<span data-ttu-id="ac9ca-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ac9ca-132">例如：</span><span class="sxs-lookup"><span data-stu-id="ac9ca-132">For example:</span></span>

<span data-ttu-id="ac9ca-133">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ac9ca-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ac9ca-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ac9ca-134">-Confirm</span></span>
<span data-ttu-id="ac9ca-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9ca-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9ca-136">-WhatIf</span></span>
<span data-ttu-id="ac9ca-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac9ca-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9ca-139">CommonParameters</span></span>
<span data-ttu-id="ac9ca-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9ca-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9ca-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ac9ca-142">INPUTS</span></span>

### <span data-ttu-id="ac9ca-143">所有</span><span class="sxs-lookup"><span data-stu-id="ac9ca-143">None</span></span>
<span data-ttu-id="ac9ca-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac9ca-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ac9ca-145">OUTPUTS</span></span>

### <span data-ttu-id="ac9ca-146">PSSnapshotUpdate 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ac9ca-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="ac9ca-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ac9ca-147">NOTES</span></span>

## <span data-ttu-id="ac9ca-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac9ca-148">RELATED LINKS</span></span>

