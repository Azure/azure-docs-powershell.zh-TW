---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967684"
---
# <span data-ttu-id="401d6-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="401d6-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="401d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="401d6-102">SYNOPSIS</span></span>
<span data-ttu-id="401d6-103">將虛擬網路遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="401d6-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="401d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="401d6-104">SYNTAX</span></span>

### <span data-ttu-id="401d6-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d6-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="401d6-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d6-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="401d6-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d6-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="401d6-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="401d6-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="401d6-109">說明</span><span class="sxs-lookup"><span data-stu-id="401d6-109">DESCRIPTION</span></span>
<span data-ttu-id="401d6-110">**AzureVirtualNetwork** Cmdlet 可將虛擬網路遷移至 Azure 資源管理器堆疊中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="401d6-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="401d6-111">示例</span><span class="sxs-lookup"><span data-stu-id="401d6-111">EXAMPLES</span></span>

### <span data-ttu-id="401d6-112">範例1：準備虛擬網路遷移</span><span class="sxs-lookup"><span data-stu-id="401d6-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="401d6-113">這個命令會準備一個名為 ContosoVNET 的虛擬網路，以遷移到 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="401d6-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="401d6-114">範例2：啟動虛擬網路遷移</span><span class="sxs-lookup"><span data-stu-id="401d6-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="401d6-115">這個命令會開始將名為 ContosoVNET 的虛擬網路遷移到 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="401d6-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="401d6-116">範例3：驗證虛擬網路遷移</span><span class="sxs-lookup"><span data-stu-id="401d6-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="401d6-117">這個命令會將名為 ContosoVNET 的虛擬網路的遷移驗證至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="401d6-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="401d6-118">參數</span><span class="sxs-lookup"><span data-stu-id="401d6-118">PARAMETERS</span></span>

### <span data-ttu-id="401d6-119">-中止</span><span class="sxs-lookup"><span data-stu-id="401d6-119">-Abort</span></span>
<span data-ttu-id="401d6-120">表示此 Cmdlet 會取消虛擬網路遷移。</span><span class="sxs-lookup"><span data-stu-id="401d6-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-121">-認可</span><span class="sxs-lookup"><span data-stu-id="401d6-121">-Commit</span></span>
<span data-ttu-id="401d6-122">表示此 Cmdlet 會啟動虛擬網路遷移。</span><span class="sxs-lookup"><span data-stu-id="401d6-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="401d6-123">-InformationAction</span></span>
<span data-ttu-id="401d6-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="401d6-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="401d6-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="401d6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="401d6-126">持續</span><span class="sxs-lookup"><span data-stu-id="401d6-126">Continue</span></span>
- <span data-ttu-id="401d6-127">理會</span><span class="sxs-lookup"><span data-stu-id="401d6-127">Ignore</span></span>
- <span data-ttu-id="401d6-128">看</span><span class="sxs-lookup"><span data-stu-id="401d6-128">Inquire</span></span>
- <span data-ttu-id="401d6-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="401d6-129">SilentlyContinue</span></span>
- <span data-ttu-id="401d6-130">停止</span><span class="sxs-lookup"><span data-stu-id="401d6-130">Stop</span></span>
- <span data-ttu-id="401d6-131">封存</span><span class="sxs-lookup"><span data-stu-id="401d6-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="401d6-132">-InformationVariable</span></span>
<span data-ttu-id="401d6-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="401d6-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-134">-準備</span><span class="sxs-lookup"><span data-stu-id="401d6-134">-Prepare</span></span>
<span data-ttu-id="401d6-135">表示這個 Cmdlet 準備用來進行遷移的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="401d6-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="401d6-136">-Profile</span></span>
<span data-ttu-id="401d6-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="401d6-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="401d6-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="401d6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-139">-驗證</span><span class="sxs-lookup"><span data-stu-id="401d6-139">-Validate</span></span>
<span data-ttu-id="401d6-140">指定此 Cmdlet 會驗證要遷移的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="401d6-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="401d6-141">-VirtualNetworkName</span></span>
<span data-ttu-id="401d6-142">要遷移的虛擬網路名稱</span><span class="sxs-lookup"><span data-stu-id="401d6-142">Name of the Virtual Network to migrate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-143">-確認</span><span class="sxs-lookup"><span data-stu-id="401d6-143">-Confirm</span></span>
<span data-ttu-id="401d6-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="401d6-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="401d6-145">-WhatIf</span></span>
<span data-ttu-id="401d6-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="401d6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="401d6-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="401d6-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="401d6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="401d6-148">CommonParameters</span></span>
<span data-ttu-id="401d6-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="401d6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="401d6-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="401d6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="401d6-151">輸入</span><span class="sxs-lookup"><span data-stu-id="401d6-151">INPUTS</span></span>

## <span data-ttu-id="401d6-152">輸出</span><span class="sxs-lookup"><span data-stu-id="401d6-152">OUTPUTS</span></span>

## <span data-ttu-id="401d6-153">筆記</span><span class="sxs-lookup"><span data-stu-id="401d6-153">NOTES</span></span>

## <span data-ttu-id="401d6-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="401d6-154">RELATED LINKS</span></span>

[<span data-ttu-id="401d6-155">移動流覽 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="401d6-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="401d6-156">移動流覽 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="401d6-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="401d6-157">移動流覽 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="401d6-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="401d6-158">移動流覽 AzureService</span><span class="sxs-lookup"><span data-stu-id="401d6-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="401d6-159">移動流覽 AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="401d6-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


