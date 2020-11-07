---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966988"
---
# <span data-ttu-id="6d2a1-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d2a1-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="6d2a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2a1-103">取得子網的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="6d2a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d2a1-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6d2a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="6d2a1-105">DESCRIPTION</span></span>
<span data-ttu-id="6d2a1-106">**AzureSubnetRouteTable** Cmdlet 會取得與子網相關聯的路由表。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="6d2a1-107">示例</span><span class="sxs-lookup"><span data-stu-id="6d2a1-107">EXAMPLES</span></span>

### <span data-ttu-id="6d2a1-108">範例1：顯示子網的路線</span><span class="sxs-lookup"><span data-stu-id="6d2a1-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="6d2a1-109">這個命令會在路由表名稱中顯示與名為 ContosoSubnet 的子網相關聯的路由。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="6d2a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="6d2a1-110">PARAMETERS</span></span>

### <span data-ttu-id="6d2a1-111">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="6d2a1-111">-Detailed</span></span>
<span data-ttu-id="6d2a1-112">表示此 Cmdlet 在與子網相關聯的路由資料表中顯示路由。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="6d2a1-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6d2a1-113">-Profile</span></span>
<span data-ttu-id="6d2a1-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6d2a1-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6d2a1-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6d2a1-116">-SubnetName</span></span>
<span data-ttu-id="6d2a1-117">指定這個 Cmdlet 取得路由資料表的子網。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="6d2a1-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6d2a1-118">-VirtualNetworkName</span></span>
<span data-ttu-id="6d2a1-119">指定包含這個 Cmdlet 取得其路由資料表之子網的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="6d2a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2a1-120">CommonParameters</span></span>
<span data-ttu-id="6d2a1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2a1-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d2a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2a1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6d2a1-123">INPUTS</span></span>

## <span data-ttu-id="6d2a1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="6d2a1-124">OUTPUTS</span></span>

## <span data-ttu-id="6d2a1-125">筆記</span><span class="sxs-lookup"><span data-stu-id="6d2a1-125">NOTES</span></span>

## <span data-ttu-id="6d2a1-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d2a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="6d2a1-127">移除-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d2a1-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="6d2a1-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6d2a1-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


