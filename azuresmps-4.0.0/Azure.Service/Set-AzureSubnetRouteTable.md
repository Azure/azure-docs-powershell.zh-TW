---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967258"
---
# <span data-ttu-id="1b56d-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b56d-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="1b56d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b56d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b56d-103">將路由資料表與子網建立關聯。</span><span class="sxs-lookup"><span data-stu-id="1b56d-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="1b56d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b56d-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1b56d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b56d-105">DESCRIPTION</span></span>
<span data-ttu-id="1b56d-106">AzureSubnetRouteTable Cmdlet 會將路由資料表與子網 **建立** 關聯。</span><span class="sxs-lookup"><span data-stu-id="1b56d-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="1b56d-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b56d-107">EXAMPLES</span></span>

### <span data-ttu-id="1b56d-108">範例1：將路由資料表與子網建立關聯</span><span class="sxs-lookup"><span data-stu-id="1b56d-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="1b56d-109">這個命令會將名為 PublicRouteTable 的路由資料表與名為 ContosoSubnet 的子網相關聯。</span><span class="sxs-lookup"><span data-stu-id="1b56d-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="1b56d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b56d-110">PARAMETERS</span></span>

### <span data-ttu-id="1b56d-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b56d-111">-PassThru</span></span>
<span data-ttu-id="1b56d-112">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="1b56d-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1b56d-113">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1b56d-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1b56d-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1b56d-114">-Profile</span></span>
<span data-ttu-id="1b56d-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1b56d-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b56d-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1b56d-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b56d-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="1b56d-117">-RouteTableName</span></span>
<span data-ttu-id="1b56d-118">指定此 Cmdlet 與子閘道聯之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b56d-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="1b56d-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1b56d-119">-SubnetName</span></span>
<span data-ttu-id="1b56d-120">指定此 Cmdlet 與路由資料表關聯的子網。</span><span class="sxs-lookup"><span data-stu-id="1b56d-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="1b56d-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1b56d-121">-VirtualNetworkName</span></span>
<span data-ttu-id="1b56d-122">指定包含此 Cmdlet 關聯路由表之子網的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="1b56d-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="1b56d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b56d-123">CommonParameters</span></span>
<span data-ttu-id="1b56d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b56d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b56d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b56d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b56d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1b56d-126">INPUTS</span></span>

## <span data-ttu-id="1b56d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1b56d-127">OUTPUTS</span></span>

## <span data-ttu-id="1b56d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1b56d-128">NOTES</span></span>

## <span data-ttu-id="1b56d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b56d-129">RELATED LINKS</span></span>

[<span data-ttu-id="1b56d-130">AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b56d-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="1b56d-131">移除-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b56d-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
