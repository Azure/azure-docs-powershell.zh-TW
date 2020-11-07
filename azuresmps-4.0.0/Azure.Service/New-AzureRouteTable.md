---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F4BADE88-28A2-42FB-9578-93D65148709E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f73e47ec25d44d3965279066de98585ae2cbaee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967435"
---
# <span data-ttu-id="23823-101">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="23823-101">New-AzureRouteTable</span></span>

## <span data-ttu-id="23823-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23823-102">SYNOPSIS</span></span>
<span data-ttu-id="23823-103">建立路由表。</span><span class="sxs-lookup"><span data-stu-id="23823-103">Creates a route table.</span></span>

## <span data-ttu-id="23823-104">句法</span><span class="sxs-lookup"><span data-stu-id="23823-104">SYNTAX</span></span>

```
New-AzureRouteTable -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="23823-105">說明</span><span class="sxs-lookup"><span data-stu-id="23823-105">DESCRIPTION</span></span>
<span data-ttu-id="23823-106">**新的-AzureRouteTable** Cmdlet 會在指定的位置建立路由表。</span><span class="sxs-lookup"><span data-stu-id="23823-106">The **New-AzureRouteTable** cmdlet creates a route table in a specified location.</span></span>
<span data-ttu-id="23823-107">您可以在路由表中新增使用者定義的路由。</span><span class="sxs-lookup"><span data-stu-id="23823-107">You can add user-defined routes to the route table.</span></span>
<span data-ttu-id="23823-108">您可以將路由資料表與虛擬網路中的子網建立關聯。</span><span class="sxs-lookup"><span data-stu-id="23823-108">You can associate the route table to a subnet in a virtual network.</span></span>

## <span data-ttu-id="23823-109">示例</span><span class="sxs-lookup"><span data-stu-id="23823-109">EXAMPLES</span></span>

## <span data-ttu-id="23823-110">參數</span><span class="sxs-lookup"><span data-stu-id="23823-110">PARAMETERS</span></span>

### <span data-ttu-id="23823-111">-標籤</span><span class="sxs-lookup"><span data-stu-id="23823-111">-Label</span></span>
<span data-ttu-id="23823-112">指定新路由資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="23823-112">Specifies a description for the new route table.</span></span>

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

### <span data-ttu-id="23823-113">-位置</span><span class="sxs-lookup"><span data-stu-id="23823-113">-Location</span></span>
<span data-ttu-id="23823-114">指定此 Cmdlet 建立路由資料表的位置。</span><span class="sxs-lookup"><span data-stu-id="23823-114">Specifies the location in which this cmdlet creates the route table.</span></span>

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

### <span data-ttu-id="23823-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="23823-115">-Name</span></span>
<span data-ttu-id="23823-116">指定此 Cmdlet 所建立之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="23823-116">Specifies a name for the route table that this cmdlet creates.</span></span>

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

### <span data-ttu-id="23823-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="23823-117">-Profile</span></span>
<span data-ttu-id="23823-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="23823-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="23823-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="23823-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23823-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23823-120">CommonParameters</span></span>
<span data-ttu-id="23823-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23823-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23823-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23823-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23823-123">輸入</span><span class="sxs-lookup"><span data-stu-id="23823-123">INPUTS</span></span>

## <span data-ttu-id="23823-124">輸出</span><span class="sxs-lookup"><span data-stu-id="23823-124">OUTPUTS</span></span>

## <span data-ttu-id="23823-125">筆記</span><span class="sxs-lookup"><span data-stu-id="23823-125">NOTES</span></span>

## <span data-ttu-id="23823-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="23823-126">RELATED LINKS</span></span>

[<span data-ttu-id="23823-127">AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="23823-127">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="23823-128">移除-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="23823-128">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


