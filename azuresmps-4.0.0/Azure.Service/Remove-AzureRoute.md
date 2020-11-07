---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967581"
---
# <span data-ttu-id="12234-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="12234-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="12234-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12234-102">SYNOPSIS</span></span>
<span data-ttu-id="12234-103">從路由表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="12234-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="12234-104">句法</span><span class="sxs-lookup"><span data-stu-id="12234-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="12234-105">說明</span><span class="sxs-lookup"><span data-stu-id="12234-105">DESCRIPTION</span></span>
<span data-ttu-id="12234-106">**AzureRoute** Cmdlet 會從路由表中移除路由。</span><span class="sxs-lookup"><span data-stu-id="12234-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="12234-107">示例</span><span class="sxs-lookup"><span data-stu-id="12234-107">EXAMPLES</span></span>

### <span data-ttu-id="12234-108">範例1：移除路線</span><span class="sxs-lookup"><span data-stu-id="12234-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="12234-109">這個命令會取得名為 ApplianceRouteTable 的路由表。</span><span class="sxs-lookup"><span data-stu-id="12234-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="12234-110">命令會將路由資料表傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12234-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="12234-111">目前的 Cmdlet 會移除名為 InternetRoute 的路由。</span><span class="sxs-lookup"><span data-stu-id="12234-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="12234-112">參數</span><span class="sxs-lookup"><span data-stu-id="12234-112">PARAMETERS</span></span>

### <span data-ttu-id="12234-113">-Force</span><span class="sxs-lookup"><span data-stu-id="12234-113">-Force</span></span>
<span data-ttu-id="12234-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="12234-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12234-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="12234-115">-Profile</span></span>
<span data-ttu-id="12234-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="12234-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="12234-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="12234-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12234-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="12234-118">-RouteName</span></span>
<span data-ttu-id="12234-119">指定此 Cmdlet 移除之新路由的名稱。</span><span class="sxs-lookup"><span data-stu-id="12234-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12234-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="12234-120">-RouteTable</span></span>
<span data-ttu-id="12234-121">指定此 Cmdlet 移除路由的路由表。</span><span class="sxs-lookup"><span data-stu-id="12234-121">Specifies the route table from which this cmdlet removes a route.</span></span>

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

### <span data-ttu-id="12234-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12234-122">CommonParameters</span></span>
<span data-ttu-id="12234-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12234-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12234-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12234-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12234-125">輸入</span><span class="sxs-lookup"><span data-stu-id="12234-125">INPUTS</span></span>

## <span data-ttu-id="12234-126">輸出</span><span class="sxs-lookup"><span data-stu-id="12234-126">OUTPUTS</span></span>

## <span data-ttu-id="12234-127">筆記</span><span class="sxs-lookup"><span data-stu-id="12234-127">NOTES</span></span>

## <span data-ttu-id="12234-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="12234-128">RELATED LINKS</span></span>

[<span data-ttu-id="12234-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="12234-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


