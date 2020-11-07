---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967269"
---
# <span data-ttu-id="8c886-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="8c886-101">Set-AzureRoute</span></span>

## <span data-ttu-id="8c886-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c886-102">SYNOPSIS</span></span>
<span data-ttu-id="8c886-103">在路由表中建立路由。</span><span class="sxs-lookup"><span data-stu-id="8c886-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="8c886-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c886-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c886-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c886-105">DESCRIPTION</span></span>
<span data-ttu-id="8c886-106">**AzureRoute** Cmdlet 會在路由表中建立路由。</span><span class="sxs-lookup"><span data-stu-id="8c886-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="8c886-107">新的路由幾乎會立即在與路由資料表相關聯的虛擬機器上生效。</span><span class="sxs-lookup"><span data-stu-id="8c886-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="8c886-108">示例</span><span class="sxs-lookup"><span data-stu-id="8c886-108">EXAMPLES</span></span>

### <span data-ttu-id="8c886-109">範例1：新增虛擬裝置的下一個躍點路由</span><span class="sxs-lookup"><span data-stu-id="8c886-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="8c886-110">這個命令會在指定的位置建立名為 ApplianceRouteTable 的路由表。</span><span class="sxs-lookup"><span data-stu-id="8c886-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="8c886-111">命令會將路由資料表傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c886-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="8c886-112">目前的 Cmdlet 會新增一個名為 ApplianceRoute03 的路由，這是一個 VirtualAppliance 的下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="8c886-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="8c886-113">此命令會指定下一個躍點 IP 位址和路由的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="8c886-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="8c886-114">範例2：新增網際網路下一個躍點路由</span><span class="sxs-lookup"><span data-stu-id="8c886-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="8c886-115">這個命令會取得名為 ApplianceRouteTable 的路由表。</span><span class="sxs-lookup"><span data-stu-id="8c886-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="8c886-116">命令會將路由資料表傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c886-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="8c886-117">目前的 Cmdlet 會新增一個名為 InternetRoute 的路由，這是網際網路的下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="8c886-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="8c886-118">此命令會指定路由的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="8c886-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="8c886-119">參數</span><span class="sxs-lookup"><span data-stu-id="8c886-119">PARAMETERS</span></span>

### <span data-ttu-id="8c886-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8c886-120">-AddressPrefix</span></span>
<span data-ttu-id="8c886-121">指定新路由的位址首碼。</span><span class="sxs-lookup"><span data-stu-id="8c886-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="8c886-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c886-122">-NextHopIpAddress</span></span>
<span data-ttu-id="8c886-123">為使用這個路線之通訊的下一個躍點指定裝置的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8c886-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="8c886-124">只有在您為 *NextHopType* 參數指定 VirtualAppliance 值時，才能指定此值。</span><span class="sxs-lookup"><span data-stu-id="8c886-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c886-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="8c886-125">-NextHopType</span></span>
<span data-ttu-id="8c886-126">指定使用此路由之流量的下一個躍點類型。</span><span class="sxs-lookup"><span data-stu-id="8c886-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="8c886-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8c886-127">Valid values are:</span></span> 

- <span data-ttu-id="8c886-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="8c886-128">VPNGateway</span></span>
- <span data-ttu-id="8c886-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="8c886-129">VNETLocal</span></span>
- <span data-ttu-id="8c886-130">互聯</span><span class="sxs-lookup"><span data-stu-id="8c886-130">Internet</span></span>
- <span data-ttu-id="8c886-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="8c886-131">VirtualAppliance</span></span>
- <span data-ttu-id="8c886-132">非</span><span class="sxs-lookup"><span data-stu-id="8c886-132">Null</span></span>

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

### <span data-ttu-id="8c886-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8c886-133">-Profile</span></span>
<span data-ttu-id="8c886-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c886-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8c886-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8c886-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c886-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8c886-136">-RouteName</span></span>
<span data-ttu-id="8c886-137">指定此 Cmdlet 所新增之新路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c886-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="8c886-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="8c886-138">-RouteTable</span></span>
<span data-ttu-id="8c886-139">指定此 Cmdlet 將新路由新增到哪個路由表。</span><span class="sxs-lookup"><span data-stu-id="8c886-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c886-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c886-140">CommonParameters</span></span>
<span data-ttu-id="8c886-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c886-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c886-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c886-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c886-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8c886-143">INPUTS</span></span>

## <span data-ttu-id="8c886-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8c886-144">OUTPUTS</span></span>

## <span data-ttu-id="8c886-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8c886-145">NOTES</span></span>

## <span data-ttu-id="8c886-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c886-146">RELATED LINKS</span></span>

[<span data-ttu-id="8c886-147">移除-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="8c886-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


