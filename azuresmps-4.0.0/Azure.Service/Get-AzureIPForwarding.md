---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967794"
---
# <span data-ttu-id="f3305-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f3305-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="f3305-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3305-102">SYNOPSIS</span></span>
<span data-ttu-id="f3305-103">取得 IP 轉寄的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3305-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="f3305-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3305-104">SYNTAX</span></span>

### <span data-ttu-id="f3305-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="f3305-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f3305-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="f3305-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f3305-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3305-107">DESCRIPTION</span></span>
<span data-ttu-id="f3305-108">**AzureIPForwarding** Cmdlet 會取得 IP 轉寄的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3305-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="f3305-109">示例</span><span class="sxs-lookup"><span data-stu-id="f3305-109">EXAMPLES</span></span>

### <span data-ttu-id="f3305-110">範例1：取得虛擬機器的 IP 轉發狀態</span><span class="sxs-lookup"><span data-stu-id="f3305-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="f3305-111">這個命令會為名為 ContosoService 的服務取得名為 ContosoVM06 的虛擬機器，並將該虛擬機器物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f3305-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="f3305-112">目前的 Cmdlet 會取得該虛擬機器的 IP 轉寄狀態。</span><span class="sxs-lookup"><span data-stu-id="f3305-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="f3305-113">參數</span><span class="sxs-lookup"><span data-stu-id="f3305-113">PARAMETERS</span></span>

### <span data-ttu-id="f3305-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f3305-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="f3305-115">指定此 Cmdlet 取得 IP 轉寄狀態的網路介面卡名稱。</span><span class="sxs-lookup"><span data-stu-id="f3305-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="f3305-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f3305-116">-Profile</span></span>
<span data-ttu-id="f3305-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f3305-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f3305-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f3305-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3305-119">-擁有方</span><span class="sxs-lookup"><span data-stu-id="f3305-119">-RoleName</span></span>
<span data-ttu-id="f3305-120">指定此 Cmdlet 取得 IP 轉寄狀態的 PaaS 角色名稱。</span><span class="sxs-lookup"><span data-stu-id="f3305-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3305-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f3305-121">-ServiceName</span></span>
<span data-ttu-id="f3305-122">指定雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3305-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="f3305-123">PaaS 角色屬於此參數指定的服務。</span><span class="sxs-lookup"><span data-stu-id="f3305-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="f3305-124">-槽</span><span class="sxs-lookup"><span data-stu-id="f3305-124">-Slot</span></span>
<span data-ttu-id="f3305-125">指定 PaaS 槽。</span><span class="sxs-lookup"><span data-stu-id="f3305-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="f3305-126">此 Cmdlet 取得轉寄狀態的 PaaS 角色具有此參數指定的槽。</span><span class="sxs-lookup"><span data-stu-id="f3305-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="f3305-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f3305-127">Valid values are:</span></span> 

- <span data-ttu-id="f3305-128">出具</span><span class="sxs-lookup"><span data-stu-id="f3305-128">Production</span></span>
- <span data-ttu-id="f3305-129">播放</span><span class="sxs-lookup"><span data-stu-id="f3305-129">Staging</span></span> 

<span data-ttu-id="f3305-130">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="f3305-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3305-131">-VM</span><span class="sxs-lookup"><span data-stu-id="f3305-131">-VM</span></span>
<span data-ttu-id="f3305-132">指定此 Cmdlet 取得 IP 轉寄狀態的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="f3305-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3305-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3305-133">CommonParameters</span></span>
<span data-ttu-id="f3305-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3305-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3305-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3305-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3305-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f3305-136">INPUTS</span></span>

## <span data-ttu-id="f3305-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f3305-137">OUTPUTS</span></span>

### <span data-ttu-id="f3305-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f3305-138">System.String</span></span>

## <span data-ttu-id="f3305-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f3305-139">NOTES</span></span>

## <span data-ttu-id="f3305-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3305-140">RELATED LINKS</span></span>

[<span data-ttu-id="f3305-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f3305-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


