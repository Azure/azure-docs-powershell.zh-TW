---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 59f01cd55083c1dcda811c8362a27ce1af69e6e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788438"
---
# <span data-ttu-id="bb2db-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="bb2db-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="bb2db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb2db-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2db-103">建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="bb2db-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="bb2db-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb2db-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb2db-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb2db-105">DESCRIPTION</span></span>
<span data-ttu-id="bb2db-106">**新的-AzSnapshotUpdateConfig** Cmdlet 會建立可設定的快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="bb2db-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="bb2db-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb2db-107">EXAMPLES</span></span>

### <span data-ttu-id="bb2db-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb2db-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="bb2db-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機空白快照更新物件。</span><span class="sxs-lookup"><span data-stu-id="bb2db-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="bb2db-110">它也會設定 Windows OS 類型，並啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="bb2db-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="bb2db-111">第二個和第三個命令會設定快照更新物件的磁片加密金鑰和金鑰加密金鑰設定。</span><span class="sxs-lookup"><span data-stu-id="bb2db-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="bb2db-112">最後一個命令會採用快照更新物件，並更新資源群組 "ResourceGroup01" 中名稱為 "Snapshot01" 的現有快照。</span><span class="sxs-lookup"><span data-stu-id="bb2db-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="bb2db-113">範例2</span><span class="sxs-lookup"><span data-stu-id="bb2db-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="bb2db-114">這個命令會將資源群組 ' ResourceGroup01 ' 中名稱為 ' Snapshot01 ' 的現有快照更新為 10 GB 磁片大小。</span><span class="sxs-lookup"><span data-stu-id="bb2db-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="bb2db-115">參數</span><span class="sxs-lookup"><span data-stu-id="bb2db-115">PARAMETERS</span></span>

### <span data-ttu-id="bb2db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2db-116">-DefaultProfile</span></span>
<span data-ttu-id="bb2db-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb2db-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb2db-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bb2db-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="bb2db-119">指定快照上的磁片加密金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="bb2db-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="bb2db-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="bb2db-120">-DiskSizeGB</span></span>
<span data-ttu-id="bb2db-121">指定磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="bb2db-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2db-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="bb2db-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="bb2db-123">啟用加密設定。</span><span class="sxs-lookup"><span data-stu-id="bb2db-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="bb2db-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bb2db-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="bb2db-125">指定快照上的金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="bb2db-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="bb2db-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="bb2db-126">-OsType</span></span>
<span data-ttu-id="bb2db-127">指定 OS 類型。</span><span class="sxs-lookup"><span data-stu-id="bb2db-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="bb2db-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bb2db-128">-SkuName</span></span>
<span data-ttu-id="bb2db-129">指定儲存空間帳戶的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="bb2db-129">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2db-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb2db-130">-Tag</span></span>
<span data-ttu-id="bb2db-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="bb2db-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bb2db-132">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bb2db-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bb2db-133">-確認</span><span class="sxs-lookup"><span data-stu-id="bb2db-133">-Confirm</span></span>
<span data-ttu-id="bb2db-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb2db-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb2db-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb2db-135">-WhatIf</span></span>
<span data-ttu-id="bb2db-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb2db-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb2db-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb2db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb2db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2db-138">CommonParameters</span></span>
<span data-ttu-id="bb2db-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb2db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2db-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb2db-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2db-141">輸入</span><span class="sxs-lookup"><span data-stu-id="bb2db-141">INPUTS</span></span>

### <span data-ttu-id="bb2db-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bb2db-142">System.String</span></span>

### <span data-ttu-id="bb2db-143">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="bb2db-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="bb2db-144">System.object</span><span class="sxs-lookup"><span data-stu-id="bb2db-144">System.Int32</span></span>

### <span data-ttu-id="bb2db-145">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bb2db-145">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bb2db-146">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb2db-146">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bb2db-147">KeyVaultAndSecretReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="bb2db-147">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="bb2db-148">KeyVaultAndKeyReference 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="bb2db-148">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="bb2db-149">輸出</span><span class="sxs-lookup"><span data-stu-id="bb2db-149">OUTPUTS</span></span>

### <span data-ttu-id="bb2db-150">PSSnapshotUpdate 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="bb2db-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="bb2db-151">筆記</span><span class="sxs-lookup"><span data-stu-id="bb2db-151">NOTES</span></span>

## <span data-ttu-id="bb2db-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb2db-152">RELATED LINKS</span></span>
