---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967598"
---
# <span data-ttu-id="ec8c7-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="ec8c7-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="ec8c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8c7-103">移除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-103">Removes a network security group.</span></span>

## <span data-ttu-id="ec8c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec8c7-104">SYNTAX</span></span>

### <span data-ttu-id="ec8c7-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="ec8c7-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec8c7-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="ec8c7-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec8c7-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="ec8c7-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec8c7-108">說明</span><span class="sxs-lookup"><span data-stu-id="ec8c7-108">DESCRIPTION</span></span>
<span data-ttu-id="ec8c7-109">**AzureNetworkSecurityGroupAssociation** Cmdlet 會從虛擬機器中移除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="ec8c7-110">示例</span><span class="sxs-lookup"><span data-stu-id="ec8c7-110">EXAMPLES</span></span>

### <span data-ttu-id="ec8c7-111">範例1：移除虛擬機器至網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="ec8c7-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="ec8c7-112">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="ec8c7-113">目前的 Cmdlet 會從該虛擬機器中移除名為 ContosoNetworkSecurityGroup 的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="ec8c7-114">參數</span><span class="sxs-lookup"><span data-stu-id="ec8c7-114">PARAMETERS</span></span>

### <span data-ttu-id="ec8c7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ec8c7-115">-Force</span></span>
<span data-ttu-id="ec8c7-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec8c7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec8c7-117">-Name</span></span>
<span data-ttu-id="ec8c7-118">指定此 Cmdlet 移除之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="ec8c7-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="ec8c7-120">指定此 Cmdlet 從中移除網路安全性群組之網路介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec8c7-121">-PassThru</span></span>
<span data-ttu-id="ec8c7-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec8c7-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec8c7-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ec8c7-124">-Profile</span></span>
<span data-ttu-id="ec8c7-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec8c7-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec8c7-127">-擁有方</span><span class="sxs-lookup"><span data-stu-id="ec8c7-127">-RoleName</span></span>
<span data-ttu-id="ec8c7-128">指定此 Cmdlet 移除網路安全性群組之 PaaS 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ec8c7-129">-ServiceName</span></span>
<span data-ttu-id="ec8c7-130">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="ec8c7-131">此 Cmdlet 移除網路安全性群組的 PaaS 角色屬於此參數指定的服務。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-132">-槽</span><span class="sxs-lookup"><span data-stu-id="ec8c7-132">-Slot</span></span>
<span data-ttu-id="ec8c7-133">指定 PaaS 槽。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="ec8c7-134">此 Cmdlet 移除網路安全性群組的 PaaS 角色具有此參數指定的槽。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="ec8c7-135">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ec8c7-135">Valid values are:</span></span>

- <span data-ttu-id="ec8c7-136">出具</span><span class="sxs-lookup"><span data-stu-id="ec8c7-136">Production</span></span>
- <span data-ttu-id="ec8c7-137">播放</span><span class="sxs-lookup"><span data-stu-id="ec8c7-137">Staging</span></span>

<span data-ttu-id="ec8c7-138">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ec8c7-139">-SubnetName</span></span>
<span data-ttu-id="ec8c7-140">指定此 Cmdlet 從中移除網路安全性群組之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ec8c7-141">-VirtualNetworkName</span></span>
<span data-ttu-id="ec8c7-142">指定包含子網的虛擬網路名稱，此 Cmdlet 會從中移除網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-143">-VM</span><span class="sxs-lookup"><span data-stu-id="ec8c7-143">-VM</span></span>
<span data-ttu-id="ec8c7-144">指定此 Cmdlet 將網路安全性群組套用到哪個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8c7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8c7-145">CommonParameters</span></span>
<span data-ttu-id="ec8c7-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8c7-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec8c7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8c7-148">輸入</span><span class="sxs-lookup"><span data-stu-id="ec8c7-148">INPUTS</span></span>

## <span data-ttu-id="ec8c7-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ec8c7-149">OUTPUTS</span></span>

### <span data-ttu-id="ec8c7-150">System.object</span><span class="sxs-lookup"><span data-stu-id="ec8c7-150">System.Boolean</span></span>

## <span data-ttu-id="ec8c7-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ec8c7-151">NOTES</span></span>

## <span data-ttu-id="ec8c7-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec8c7-152">RELATED LINKS</span></span>

[<span data-ttu-id="ec8c7-153">AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="ec8c7-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="ec8c7-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="ec8c7-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
