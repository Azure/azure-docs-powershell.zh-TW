---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967402"
---
# <span data-ttu-id="5f9ae-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="5f9ae-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="5f9ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9ae-103">啟用或停用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="5f9ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f9ae-104">SYNTAX</span></span>

### <span data-ttu-id="5f9ae-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="5f9ae-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f9ae-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="5f9ae-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f9ae-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="5f9ae-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f9ae-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="5f9ae-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5f9ae-109">說明</span><span class="sxs-lookup"><span data-stu-id="5f9ae-109">DESCRIPTION</span></span>
<span data-ttu-id="5f9ae-110">**AzureIPForwarding** Cmdlet 會針對虛擬機器啟用或停用 IP 轉寄，對於平臺為服務 (PaaS) 角色，或是屬於虛擬機器或 PaaS 角色的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="5f9ae-111">示例</span><span class="sxs-lookup"><span data-stu-id="5f9ae-111">EXAMPLES</span></span>

### <span data-ttu-id="5f9ae-112">範例1：啟用虛擬機器的 IP 轉寄功能</span><span class="sxs-lookup"><span data-stu-id="5f9ae-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="5f9ae-113">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="5f9ae-114">目前的 Cmdlet 可為該虛擬機器啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="5f9ae-115">範例2：停用虛擬機器的 IP 轉寄功能</span><span class="sxs-lookup"><span data-stu-id="5f9ae-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="5f9ae-116">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="5f9ae-117">目前的 Cmdlet 會停用該虛擬機器的 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="5f9ae-118">參數</span><span class="sxs-lookup"><span data-stu-id="5f9ae-118">PARAMETERS</span></span>

### <span data-ttu-id="5f9ae-119">-停用</span><span class="sxs-lookup"><span data-stu-id="5f9ae-119">-Disable</span></span>
<span data-ttu-id="5f9ae-120">表示此 Cmdlet 會停用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9ae-121">-啟用</span><span class="sxs-lookup"><span data-stu-id="5f9ae-121">-Enable</span></span>
<span data-ttu-id="5f9ae-122">表示此 Cmdlet 啟用 IP 轉寄。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9ae-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5f9ae-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="5f9ae-124">指定此 Cmdlet 設定 IP 轉寄之網路介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="5f9ae-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f9ae-125">-PassThru</span></span>
<span data-ttu-id="5f9ae-126">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5f9ae-127">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5f9ae-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5f9ae-128">-Profile</span></span>
<span data-ttu-id="5f9ae-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f9ae-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f9ae-131">-擁有方</span><span class="sxs-lookup"><span data-stu-id="5f9ae-131">-RoleName</span></span>
<span data-ttu-id="5f9ae-132">指定此 Cmdlet 設定 IP 轉寄之 PaaS 角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9ae-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5f9ae-133">-ServiceName</span></span>
<span data-ttu-id="5f9ae-134">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="5f9ae-135">PaaS 角色屬於此參數指定的服務。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f9ae-136">-槽</span><span class="sxs-lookup"><span data-stu-id="5f9ae-136">-Slot</span></span>
<span data-ttu-id="5f9ae-137">指定 PaaS 槽。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="5f9ae-138">此 Cmdlet 設定轉寄的 PaaS 角色具有此參數指定的槽。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="5f9ae-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="5f9ae-139">Valid values are:</span></span>

- <span data-ttu-id="5f9ae-140">出具</span><span class="sxs-lookup"><span data-stu-id="5f9ae-140">Production</span></span>
- <span data-ttu-id="5f9ae-141">播放</span><span class="sxs-lookup"><span data-stu-id="5f9ae-141">Staging</span></span>

<span data-ttu-id="5f9ae-142">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9ae-143">-VM</span><span class="sxs-lookup"><span data-stu-id="5f9ae-143">-VM</span></span>
<span data-ttu-id="5f9ae-144">指定此 Cmdlet 設定 IP 轉寄的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9ae-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9ae-145">CommonParameters</span></span>
<span data-ttu-id="5f9ae-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9ae-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f9ae-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9ae-148">輸入</span><span class="sxs-lookup"><span data-stu-id="5f9ae-148">INPUTS</span></span>

## <span data-ttu-id="5f9ae-149">輸出</span><span class="sxs-lookup"><span data-stu-id="5f9ae-149">OUTPUTS</span></span>

### <span data-ttu-id="5f9ae-150">System.object</span><span class="sxs-lookup"><span data-stu-id="5f9ae-150">System.Boolean</span></span>

## <span data-ttu-id="5f9ae-151">筆記</span><span class="sxs-lookup"><span data-stu-id="5f9ae-151">NOTES</span></span>

## <span data-ttu-id="5f9ae-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f9ae-152">RELATED LINKS</span></span>

[<span data-ttu-id="5f9ae-153">AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="5f9ae-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
