---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 58329D8A-CB54-46FB-84A7-C31F00C13827
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6333430682de7693b6b87f9d037dea66725bfed8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967578"
---
# <span data-ttu-id="7d0db-101">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d0db-101">Remove-AzureRouteTable</span></span>

## <span data-ttu-id="7d0db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d0db-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0db-103">移除路由表。</span><span class="sxs-lookup"><span data-stu-id="7d0db-103">Removes a route table.</span></span>

## <span data-ttu-id="7d0db-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d0db-104">SYNTAX</span></span>

```
Remove-AzureRouteTable -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d0db-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d0db-105">DESCRIPTION</span></span>
<span data-ttu-id="7d0db-106">**AzureRouteTable** Cmdlet 會從您的訂閱中移除路由表。</span><span class="sxs-lookup"><span data-stu-id="7d0db-106">The **Remove-AzureRouteTable** cmdlet removes a route table from your subscription.</span></span>
<span data-ttu-id="7d0db-107">如果路由資料表與子網相關聯，您就無法移除該資料表。</span><span class="sxs-lookup"><span data-stu-id="7d0db-107">If a route table is associated to a subnet, you cannot remove the table.</span></span>

## <span data-ttu-id="7d0db-108">示例</span><span class="sxs-lookup"><span data-stu-id="7d0db-108">EXAMPLES</span></span>

### <span data-ttu-id="7d0db-109">範例1：移除路由資料表</span><span class="sxs-lookup"><span data-stu-id="7d0db-109">Example 1: Remove a route table</span></span>
```
PS C:\> Remove-AzureRouteTable -Name "PublicRouteTable"
```

<span data-ttu-id="7d0db-110">這個命令會移除名為 PublicRouteTable 的路由表。</span><span class="sxs-lookup"><span data-stu-id="7d0db-110">This command removes the route table named PublicRouteTable.</span></span>

## <span data-ttu-id="7d0db-111">參數</span><span class="sxs-lookup"><span data-stu-id="7d0db-111">PARAMETERS</span></span>

### <span data-ttu-id="7d0db-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7d0db-112">-Force</span></span>
<span data-ttu-id="7d0db-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7d0db-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d0db-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d0db-114">-Name</span></span>
<span data-ttu-id="7d0db-115">指定此 Cmdlet 移除之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d0db-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d0db-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d0db-116">-PassThru</span></span>
<span data-ttu-id="7d0db-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7d0db-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d0db-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7d0db-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d0db-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7d0db-119">-Profile</span></span>
<span data-ttu-id="7d0db-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7d0db-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d0db-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7d0db-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d0db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0db-122">CommonParameters</span></span>
<span data-ttu-id="7d0db-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d0db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0db-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d0db-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0db-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7d0db-125">INPUTS</span></span>

## <span data-ttu-id="7d0db-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7d0db-126">OUTPUTS</span></span>

## <span data-ttu-id="7d0db-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7d0db-127">NOTES</span></span>

## <span data-ttu-id="7d0db-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d0db-128">RELATED LINKS</span></span>

[<span data-ttu-id="7d0db-129">AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d0db-129">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="7d0db-130">新-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d0db-130">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)
