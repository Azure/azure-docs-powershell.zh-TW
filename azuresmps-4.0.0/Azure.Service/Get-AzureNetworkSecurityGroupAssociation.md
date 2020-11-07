---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968028"
---
# <span data-ttu-id="82c95-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="82c95-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="82c95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82c95-102">SYNOPSIS</span></span>
<span data-ttu-id="82c95-103">取得虛擬機器、網路介面卡或 PaaS 角色的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="82c95-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="82c95-104">句法</span><span class="sxs-lookup"><span data-stu-id="82c95-104">SYNTAX</span></span>

### <span data-ttu-id="82c95-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="82c95-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82c95-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="82c95-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="82c95-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="82c95-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82c95-108">說明</span><span class="sxs-lookup"><span data-stu-id="82c95-108">DESCRIPTION</span></span>
<span data-ttu-id="82c95-109">**AzureNetworkSecurityGroupAssociation** Cmdlet 會取得虛擬機器、網路介面卡或平臺作為服務 (PaaS) 角色的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="82c95-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="82c95-110">示例</span><span class="sxs-lookup"><span data-stu-id="82c95-110">EXAMPLES</span></span>

### <span data-ttu-id="82c95-111">範例1：取得虛擬機器的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="82c95-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="82c95-112">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82c95-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="82c95-113">目前的 Cmdlet 會取得與該虛擬機器相關聯的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="82c95-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="82c95-114">參數</span><span class="sxs-lookup"><span data-stu-id="82c95-114">PARAMETERS</span></span>

### <span data-ttu-id="82c95-115">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="82c95-115">-Detailed</span></span>
<span data-ttu-id="82c95-116">表示此 Cmdlet 會傳回與虛擬機器相關聯之網路安全性群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="82c95-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="82c95-117">這些詳細資料包括位置與規則。</span><span class="sxs-lookup"><span data-stu-id="82c95-117">These details include location and rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="82c95-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="82c95-119">指定此 Cmdlet 取得網路安全性群組之網路介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="82c95-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="82c95-120">-Profile</span></span>
<span data-ttu-id="82c95-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="82c95-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="82c95-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="82c95-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82c95-123">-擁有方</span><span class="sxs-lookup"><span data-stu-id="82c95-123">-RoleName</span></span>
<span data-ttu-id="82c95-124">指定此 Cmdlet 取得網路安全性群組之 PaaS 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="82c95-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="82c95-125">-ServiceName</span></span>
<span data-ttu-id="82c95-126">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="82c95-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="82c95-127">PaaS 角色屬於此參數指定的服務。</span><span class="sxs-lookup"><span data-stu-id="82c95-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-128">-槽</span><span class="sxs-lookup"><span data-stu-id="82c95-128">-Slot</span></span>
<span data-ttu-id="82c95-129">指定 PaaS 槽。</span><span class="sxs-lookup"><span data-stu-id="82c95-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="82c95-130">此 Cmdlet 取得網路安全性群組的 PaaS 角色具有此參數指定的槽。</span><span class="sxs-lookup"><span data-stu-id="82c95-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="82c95-131">有效值為：</span><span class="sxs-lookup"><span data-stu-id="82c95-131">Valid values are:</span></span> 

- <span data-ttu-id="82c95-132">出具</span><span class="sxs-lookup"><span data-stu-id="82c95-132">Production</span></span>
- <span data-ttu-id="82c95-133">播放</span><span class="sxs-lookup"><span data-stu-id="82c95-133">Staging</span></span> 

<span data-ttu-id="82c95-134">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="82c95-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="82c95-135">-SubnetName</span></span>
<span data-ttu-id="82c95-136">指定此 Cmdlet 取得網路安全性群組之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="82c95-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="82c95-137">-VirtualNetworkName</span></span>
<span data-ttu-id="82c95-138">指定包含此 Cmdlet 取得網路安全性群組之子網的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="82c95-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-139">-VM</span><span class="sxs-lookup"><span data-stu-id="82c95-139">-VM</span></span>
<span data-ttu-id="82c95-140">指定此 Cmdlet 將網路安全性群組套用到哪個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="82c95-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82c95-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c95-141">CommonParameters</span></span>
<span data-ttu-id="82c95-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82c95-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c95-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82c95-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c95-144">輸入</span><span class="sxs-lookup"><span data-stu-id="82c95-144">INPUTS</span></span>

## <span data-ttu-id="82c95-145">輸出</span><span class="sxs-lookup"><span data-stu-id="82c95-145">OUTPUTS</span></span>

### <span data-ttu-id="82c95-146">NetworkSecurityGroup. ServiceManagement. INetworkSecurityGroup （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="82c95-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="82c95-147">筆記</span><span class="sxs-lookup"><span data-stu-id="82c95-147">NOTES</span></span>

## <span data-ttu-id="82c95-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="82c95-148">RELATED LINKS</span></span>

[<span data-ttu-id="82c95-149">移除-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="82c95-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="82c95-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="82c95-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


