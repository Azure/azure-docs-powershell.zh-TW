---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967759"
---
# <span data-ttu-id="c2b61-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2b61-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="c2b61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2b61-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b61-103">取得路由表。</span><span class="sxs-lookup"><span data-stu-id="c2b61-103">Gets a route table.</span></span>

## <span data-ttu-id="c2b61-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2b61-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c2b61-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2b61-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b61-106">**AzureRouteTable** Cmdlet 會取得路由表。</span><span class="sxs-lookup"><span data-stu-id="c2b61-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="c2b61-107">指定 *詳細* 的參數，以列出路由資料表中的路由。</span><span class="sxs-lookup"><span data-stu-id="c2b61-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="c2b61-108">示例</span><span class="sxs-lookup"><span data-stu-id="c2b61-108">EXAMPLES</span></span>

### <span data-ttu-id="c2b61-109">範例1：取得路由資料表的詳細資料</span><span class="sxs-lookup"><span data-stu-id="c2b61-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="c2b61-110">這個命令會取得名為 ApplianceRouteTable 的路由資料表的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c2b61-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="c2b61-111">參數</span><span class="sxs-lookup"><span data-stu-id="c2b61-111">PARAMETERS</span></span>

### <span data-ttu-id="c2b61-112">-詳細資訊</span><span class="sxs-lookup"><span data-stu-id="c2b61-112">-Detailed</span></span>
<span data-ttu-id="c2b61-113">表示此 Cmdlet 在路由表中顯示路由。</span><span class="sxs-lookup"><span data-stu-id="c2b61-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="c2b61-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2b61-114">-Name</span></span>
<span data-ttu-id="c2b61-115">指定此 Cmdlet 所取得之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2b61-115">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c2b61-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c2b61-116">-Profile</span></span>
<span data-ttu-id="c2b61-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c2b61-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c2b61-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c2b61-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2b61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b61-119">CommonParameters</span></span>
<span data-ttu-id="c2b61-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2b61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b61-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2b61-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b61-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c2b61-122">INPUTS</span></span>

## <span data-ttu-id="c2b61-123">輸出</span><span class="sxs-lookup"><span data-stu-id="c2b61-123">OUTPUTS</span></span>

## <span data-ttu-id="c2b61-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c2b61-124">NOTES</span></span>

## <span data-ttu-id="c2b61-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2b61-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2b61-126">新-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2b61-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="c2b61-127">移除-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c2b61-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


