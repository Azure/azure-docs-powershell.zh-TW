---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967902"
---
# <span data-ttu-id="51006-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="51006-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="51006-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51006-102">SYNOPSIS</span></span>
<span data-ttu-id="51006-103">從子網上移除路由資料表關聯。</span><span class="sxs-lookup"><span data-stu-id="51006-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="51006-104">句法</span><span class="sxs-lookup"><span data-stu-id="51006-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51006-105">說明</span><span class="sxs-lookup"><span data-stu-id="51006-105">DESCRIPTION</span></span>
<span data-ttu-id="51006-106">**AzureSubnetRouteTable** Cmdlet 會從子網中移除路由表關聯。</span><span class="sxs-lookup"><span data-stu-id="51006-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="51006-107">示例</span><span class="sxs-lookup"><span data-stu-id="51006-107">EXAMPLES</span></span>

### <span data-ttu-id="51006-108">範例1：移除路由資料表與子網之間的關聯</span><span class="sxs-lookup"><span data-stu-id="51006-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="51006-109">這個命令會移除名為 PublicRouteTable 的路由資料表與名為 ContosoSubnet 的子網之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="51006-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="51006-110">參數</span><span class="sxs-lookup"><span data-stu-id="51006-110">PARAMETERS</span></span>

### <span data-ttu-id="51006-111">-Force</span><span class="sxs-lookup"><span data-stu-id="51006-111">-Force</span></span>
<span data-ttu-id="51006-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="51006-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51006-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51006-113">-PassThru</span></span>
<span data-ttu-id="51006-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="51006-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="51006-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="51006-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51006-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="51006-116">-Profile</span></span>
<span data-ttu-id="51006-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="51006-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="51006-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="51006-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51006-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="51006-119">-SubnetName</span></span>
<span data-ttu-id="51006-120">指定此 Cmdlet 移除路由資料表的子網。</span><span class="sxs-lookup"><span data-stu-id="51006-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="51006-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="51006-121">-VirtualNetworkName</span></span>
<span data-ttu-id="51006-122">指定包含此 Cmdlet 將其移除路由表之子網的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="51006-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="51006-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51006-123">CommonParameters</span></span>
<span data-ttu-id="51006-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51006-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51006-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51006-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51006-126">輸入</span><span class="sxs-lookup"><span data-stu-id="51006-126">INPUTS</span></span>

## <span data-ttu-id="51006-127">輸出</span><span class="sxs-lookup"><span data-stu-id="51006-127">OUTPUTS</span></span>

## <span data-ttu-id="51006-128">筆記</span><span class="sxs-lookup"><span data-stu-id="51006-128">NOTES</span></span>

## <span data-ttu-id="51006-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="51006-129">RELATED LINKS</span></span>

[<span data-ttu-id="51006-130">AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="51006-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="51006-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="51006-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


