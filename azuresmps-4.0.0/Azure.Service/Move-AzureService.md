---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967686"
---
# <span data-ttu-id="a3902-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="a3902-101">Move-AzureService</span></span>

## <span data-ttu-id="a3902-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3902-102">SYNOPSIS</span></span>
<span data-ttu-id="a3902-103">將雲端服務遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a3902-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3902-104">SYNTAX</span></span>

### <span data-ttu-id="a3902-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3902-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3902-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3902-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3902-107">PrepareNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3902-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3902-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3902-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3902-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3902-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3902-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3902-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3902-111">說明</span><span class="sxs-lookup"><span data-stu-id="a3902-111">DESCRIPTION</span></span>
<span data-ttu-id="a3902-112">**AzureService** Cmdlet 會將雲端服務和該服務內的部署遷移至 Azure 資源管理器堆疊中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a3902-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a3902-113">示例</span><span class="sxs-lookup"><span data-stu-id="a3902-113">EXAMPLES</span></span>

### <span data-ttu-id="a3902-114">範例1：準備服務遷移</span><span class="sxs-lookup"><span data-stu-id="a3902-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="a3902-115">這個命令會準備一個名為 ContosoService 的服務，以遷移到 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a3902-116">遷移包括名為 ContosoVM 的部署。</span><span class="sxs-lookup"><span data-stu-id="a3902-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a3902-117">範例2：啟動服務遷移</span><span class="sxs-lookup"><span data-stu-id="a3902-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="a3902-118">這個命令會開始將名為 ContosoService 的服務遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a3902-119">遷移包括名為 ContosoVM 的部署。</span><span class="sxs-lookup"><span data-stu-id="a3902-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a3902-120">範例3：取消服務遷移</span><span class="sxs-lookup"><span data-stu-id="a3902-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="a3902-121">這個命令會取消將名為 ContosoService 的服務遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="a3902-122">範例4：準備服務遷移至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a3902-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="a3902-123">這個命令會準備一個名為 ContosoService 的服務，以遷移到 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a3902-124">遷移包括名為 ContosoVM 的部署。</span><span class="sxs-lookup"><span data-stu-id="a3902-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="a3902-125">遷移使用先前建立的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a3902-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="a3902-126">範例5：驗證服務遷移</span><span class="sxs-lookup"><span data-stu-id="a3902-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="a3902-127">這個命令會將名為 ContosoService 的服務的遷移驗證至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a3902-128">遷移包括名為 ContosoVM 的部署。</span><span class="sxs-lookup"><span data-stu-id="a3902-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a3902-129">範例6：驗證服務遷移至現有的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="a3902-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="a3902-130">這個命令會將名為 ContosoService 的服務的遷移驗證至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="a3902-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a3902-131">遷移包括名為 ContosoVM 的部署。</span><span class="sxs-lookup"><span data-stu-id="a3902-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="a3902-132">遷移使用先前建立的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a3902-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="a3902-133">參數</span><span class="sxs-lookup"><span data-stu-id="a3902-133">PARAMETERS</span></span>

### <span data-ttu-id="a3902-134">-中止</span><span class="sxs-lookup"><span data-stu-id="a3902-134">-Abort</span></span>
<span data-ttu-id="a3902-135">表示此 Cmdlet 會取消服務遷移。</span><span class="sxs-lookup"><span data-stu-id="a3902-135">Indicates that this cmdlet cancels the service migration.</span></span>

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

### <span data-ttu-id="a3902-136">-認可</span><span class="sxs-lookup"><span data-stu-id="a3902-136">-Commit</span></span>
<span data-ttu-id="a3902-137">表示此 Cmdlet 會啟動服務遷移。</span><span class="sxs-lookup"><span data-stu-id="a3902-137">Indicates that this cmdlet starts the service migration.</span></span>

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

### <span data-ttu-id="a3902-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3902-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="a3902-139">表示此 Cmdlet 在 Azure 資源管理器堆疊中建立虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a3902-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a3902-140">-DeploymentName</span></span>
<span data-ttu-id="a3902-141">指定此 Cmdlet 遷移之雲端服務部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3902-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-142">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a3902-142">-InformationAction</span></span>
<span data-ttu-id="a3902-143">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a3902-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a3902-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a3902-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a3902-145">持續</span><span class="sxs-lookup"><span data-stu-id="a3902-145">Continue</span></span>
- <span data-ttu-id="a3902-146">理會</span><span class="sxs-lookup"><span data-stu-id="a3902-146">Ignore</span></span>
- <span data-ttu-id="a3902-147">看</span><span class="sxs-lookup"><span data-stu-id="a3902-147">Inquire</span></span>
- <span data-ttu-id="a3902-148">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a3902-148">SilentlyContinue</span></span>
- <span data-ttu-id="a3902-149">停止</span><span class="sxs-lookup"><span data-stu-id="a3902-149">Stop</span></span>
- <span data-ttu-id="a3902-150">封存</span><span class="sxs-lookup"><span data-stu-id="a3902-150">Suspend</span></span>

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

### <span data-ttu-id="a3902-151">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a3902-151">-InformationVariable</span></span>
<span data-ttu-id="a3902-152">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a3902-152">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a3902-153">-準備</span><span class="sxs-lookup"><span data-stu-id="a3902-153">-Prepare</span></span>
<span data-ttu-id="a3902-154">表示此 Cmdlet 會為遷移準備雲端服務。</span><span class="sxs-lookup"><span data-stu-id="a3902-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-155">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a3902-155">-Profile</span></span>
<span data-ttu-id="a3902-156">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3902-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3902-157">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a3902-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3902-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a3902-158">-ServiceName</span></span>
<span data-ttu-id="a3902-159">指定此 Cmdlet 所遷移之雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3902-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="a3902-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a3902-160">-SubnetName</span></span>
<span data-ttu-id="a3902-161">指定虛擬網路內子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3902-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3902-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="a3902-163">表示此 Cmdlet 會將雲端服務遷移到 Azure 資源管理器堆疊中的現有虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="a3902-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-164">-驗證</span><span class="sxs-lookup"><span data-stu-id="a3902-164">-Validate</span></span>
<span data-ttu-id="a3902-165">指定此 Cmdlet 會驗證雲端服務以進行遷移。</span><span class="sxs-lookup"><span data-stu-id="a3902-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a3902-166">-VirtualNetworkName</span></span>
<span data-ttu-id="a3902-167">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3902-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3902-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="a3902-169">指定現有虛擬網路之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3902-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3902-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3902-170">CommonParameters</span></span>
<span data-ttu-id="a3902-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3902-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3902-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3902-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3902-173">輸入</span><span class="sxs-lookup"><span data-stu-id="a3902-173">INPUTS</span></span>

## <span data-ttu-id="a3902-174">輸出</span><span class="sxs-lookup"><span data-stu-id="a3902-174">OUTPUTS</span></span>

## <span data-ttu-id="a3902-175">筆記</span><span class="sxs-lookup"><span data-stu-id="a3902-175">NOTES</span></span>

## <span data-ttu-id="a3902-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3902-176">RELATED LINKS</span></span>

[<span data-ttu-id="a3902-177">移動流覽 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a3902-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="a3902-178">移動流覽 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="a3902-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="a3902-179">移動流覽 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3902-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="a3902-180">移動流覽 AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3902-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="a3902-181">移動流覽 AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a3902-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


