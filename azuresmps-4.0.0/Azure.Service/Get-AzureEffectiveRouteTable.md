---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967799"
---
# <span data-ttu-id="bab21-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="bab21-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="bab21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bab21-102">SYNOPSIS</span></span>
<span data-ttu-id="bab21-103">取得在虛擬機器中套用的路線。</span><span class="sxs-lookup"><span data-stu-id="bab21-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="bab21-104">句法</span><span class="sxs-lookup"><span data-stu-id="bab21-104">SYNTAX</span></span>

### <span data-ttu-id="bab21-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="bab21-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bab21-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="bab21-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bab21-107">說明</span><span class="sxs-lookup"><span data-stu-id="bab21-107">DESCRIPTION</span></span>
<span data-ttu-id="bab21-108">**AzureEffectiveRouteTable** Cmdlet 會取得在虛擬機器中套用的路由。</span><span class="sxs-lookup"><span data-stu-id="bab21-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="bab21-109">這個作業可能需要幾秒鐘的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="bab21-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="bab21-110">示例</span><span class="sxs-lookup"><span data-stu-id="bab21-110">EXAMPLES</span></span>

### <span data-ttu-id="bab21-111">範例1：取得已套用虛擬機器的有效路線</span><span class="sxs-lookup"><span data-stu-id="bab21-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="bab21-112">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bab21-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="bab21-113">目前的 Cmdlet 會取得套用到該虛擬機器的路由。</span><span class="sxs-lookup"><span data-stu-id="bab21-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="bab21-114">參數</span><span class="sxs-lookup"><span data-stu-id="bab21-114">PARAMETERS</span></span>

### <span data-ttu-id="bab21-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="bab21-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="bab21-116">指定此 Cmdlet 取得有效路由的網路介面卡名稱。</span><span class="sxs-lookup"><span data-stu-id="bab21-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab21-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bab21-117">-Profile</span></span>
<span data-ttu-id="bab21-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bab21-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bab21-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bab21-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bab21-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="bab21-120">-RoleInstanceName</span></span>
<span data-ttu-id="bab21-121">指定此 Cmdlet 取得有效路由的 PaaS 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="bab21-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bab21-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bab21-122">-ServiceName</span></span>
<span data-ttu-id="bab21-123">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="bab21-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="bab21-124">此 Cmdlet 取得其有效路由的 PaaS 角色，屬於此參數指定的服務。</span><span class="sxs-lookup"><span data-stu-id="bab21-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="bab21-125">-槽</span><span class="sxs-lookup"><span data-stu-id="bab21-125">-Slot</span></span>
<span data-ttu-id="bab21-126">指定 PaaS 槽。</span><span class="sxs-lookup"><span data-stu-id="bab21-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="bab21-127">此 Cmdlet 取得有效路由的 PaaS 角色具有此參數指定的槽。</span><span class="sxs-lookup"><span data-stu-id="bab21-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="bab21-128">有效值為：</span><span class="sxs-lookup"><span data-stu-id="bab21-128">Valid values are:</span></span> 

- <span data-ttu-id="bab21-129">出具</span><span class="sxs-lookup"><span data-stu-id="bab21-129">Production</span></span>
- <span data-ttu-id="bab21-130">播放</span><span class="sxs-lookup"><span data-stu-id="bab21-130">Staging</span></span> 

<span data-ttu-id="bab21-131">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="bab21-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab21-132">-VM</span><span class="sxs-lookup"><span data-stu-id="bab21-132">-VM</span></span>
<span data-ttu-id="bab21-133">指定此 Cmdlet 取得有效路由的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="bab21-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bab21-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab21-134">CommonParameters</span></span>
<span data-ttu-id="bab21-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bab21-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab21-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bab21-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab21-137">輸入</span><span class="sxs-lookup"><span data-stu-id="bab21-137">INPUTS</span></span>

## <span data-ttu-id="bab21-138">輸出</span><span class="sxs-lookup"><span data-stu-id="bab21-138">OUTPUTS</span></span>

### <span data-ttu-id="bab21-139">WindowsAzure （EffectiveRouteTable，WindowsAzure. Network.. 網路> 的網路上的。<</span><span class="sxs-lookup"><span data-stu-id="bab21-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="bab21-140">筆記</span><span class="sxs-lookup"><span data-stu-id="bab21-140">NOTES</span></span>

## <span data-ttu-id="bab21-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="bab21-141">RELATED LINKS</span></span>

[<span data-ttu-id="bab21-142">AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bab21-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="bab21-143">新-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bab21-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="bab21-144">移除-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="bab21-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="bab21-145">移除-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="bab21-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="bab21-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="bab21-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


