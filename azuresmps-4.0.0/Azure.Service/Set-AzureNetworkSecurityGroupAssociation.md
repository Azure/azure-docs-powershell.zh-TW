---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967204"
---
# <span data-ttu-id="cd0e5-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="cd0e5-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="cd0e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0e5-103">將網路安全性群組與虛擬機器、PaaS 角色或網路介面卡建立關聯。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="cd0e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd0e5-104">SYNTAX</span></span>

### <span data-ttu-id="cd0e5-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="cd0e5-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cd0e5-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="cd0e5-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cd0e5-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="cd0e5-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd0e5-108">說明</span><span class="sxs-lookup"><span data-stu-id="cd0e5-108">DESCRIPTION</span></span>
<span data-ttu-id="cd0e5-109">**AzureNetworkSecurityGroupAssociation** Cmdlet 會將網路安全性群組與虛擬機器、platform 作為服務 (PaaS) 角色或網路介面卡相關聯。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="cd0e5-110">示例</span><span class="sxs-lookup"><span data-stu-id="cd0e5-110">EXAMPLES</span></span>

### <span data-ttu-id="cd0e5-111">範例1：指派虛擬機器至網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="cd0e5-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="cd0e5-112">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="cd0e5-113">目前的 Cmdlet 會將名為 ContosoNetworkSecurityGroup 的網路安全性群組指派給該虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="cd0e5-114">參數</span><span class="sxs-lookup"><span data-stu-id="cd0e5-114">PARAMETERS</span></span>

### <span data-ttu-id="cd0e5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd0e5-115">-Force</span></span>
<span data-ttu-id="cd0e5-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cd0e5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd0e5-117">-Name</span></span>
<span data-ttu-id="cd0e5-118">指定此 Cmdlet 所設定之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="cd0e5-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="cd0e5-120">指定此 Cmdlet 套用網路安全性群組之網路介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd0e5-121">-PassThru</span></span>
<span data-ttu-id="cd0e5-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cd0e5-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd0e5-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cd0e5-124">-Profile</span></span>
<span data-ttu-id="cd0e5-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cd0e5-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd0e5-127">-擁有方</span><span class="sxs-lookup"><span data-stu-id="cd0e5-127">-RoleName</span></span>
<span data-ttu-id="cd0e5-128">指定此 Cmdlet 套用網路安全性群組之 PaaS 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cd0e5-129">-ServiceName</span></span>
<span data-ttu-id="cd0e5-130">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="cd0e5-131">PaaS 角色屬於此參數指定的服務。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-132">-槽</span><span class="sxs-lookup"><span data-stu-id="cd0e5-132">-Slot</span></span>
<span data-ttu-id="cd0e5-133">指定 PaaS 槽。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="cd0e5-134">此 Cmdlet 為其設定網路安全群組的 PaaS 角色具有此參數指定的槽。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="cd0e5-135">有效值為：</span><span class="sxs-lookup"><span data-stu-id="cd0e5-135">Valid values are:</span></span> 

- <span data-ttu-id="cd0e5-136">出具</span><span class="sxs-lookup"><span data-stu-id="cd0e5-136">Production</span></span>
- <span data-ttu-id="cd0e5-137">播放</span><span class="sxs-lookup"><span data-stu-id="cd0e5-137">Staging</span></span> 

<span data-ttu-id="cd0e5-138">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cd0e5-139">-SubnetName</span></span>
<span data-ttu-id="cd0e5-140">指定此 Cmdlet 要與網路安全群組相關聯之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cd0e5-141">-VirtualNetworkName</span></span>
<span data-ttu-id="cd0e5-142">指定包含此 Cmdlet 將其與網路安全群組相關聯之子網之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-143">-VM</span><span class="sxs-lookup"><span data-stu-id="cd0e5-143">-VM</span></span>
<span data-ttu-id="cd0e5-144">指定此 Cmdlet 將網路安全性群組套用到哪個虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd0e5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0e5-145">CommonParameters</span></span>
<span data-ttu-id="cd0e5-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0e5-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd0e5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0e5-148">輸入</span><span class="sxs-lookup"><span data-stu-id="cd0e5-148">INPUTS</span></span>

## <span data-ttu-id="cd0e5-149">輸出</span><span class="sxs-lookup"><span data-stu-id="cd0e5-149">OUTPUTS</span></span>

### <span data-ttu-id="cd0e5-150">System.object</span><span class="sxs-lookup"><span data-stu-id="cd0e5-150">System.Boolean</span></span>

## <span data-ttu-id="cd0e5-151">筆記</span><span class="sxs-lookup"><span data-stu-id="cd0e5-151">NOTES</span></span>

## <span data-ttu-id="cd0e5-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd0e5-152">RELATED LINKS</span></span>

[<span data-ttu-id="cd0e5-153">AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="cd0e5-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="cd0e5-154">移除-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="cd0e5-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

