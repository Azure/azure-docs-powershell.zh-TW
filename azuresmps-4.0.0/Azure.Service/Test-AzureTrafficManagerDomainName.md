---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967381"
---
# <span data-ttu-id="e729f-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="e729f-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="e729f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e729f-102">SYNOPSIS</span></span>
<span data-ttu-id="e729f-103">檢查是否可使用 [流量管理器] 設定檔的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e729f-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="e729f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e729f-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e729f-105">說明</span><span class="sxs-lookup"><span data-stu-id="e729f-105">DESCRIPTION</span></span>
<span data-ttu-id="e729f-106">**AzureTrafficManagerDomainName** Cmdlet 會檢查功能變數名稱是否可做為 Microsoft Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="e729f-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="e729f-107">如果有可用的功能變數名稱，這個 Cmdlet 會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="e729f-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="e729f-108">示例</span><span class="sxs-lookup"><span data-stu-id="e729f-108">EXAMPLES</span></span>

### <span data-ttu-id="e729f-109">範例1：檢查是否有可用的功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="e729f-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="e729f-110">這個命令會檢查是否可使用 [網功能變數名稱稱 ContosoApp.trafficmanager.net] 做為流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="e729f-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="e729f-111">參數</span><span class="sxs-lookup"><span data-stu-id="e729f-111">PARAMETERS</span></span>

### <span data-ttu-id="e729f-112">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="e729f-112">-DomainName</span></span>
<span data-ttu-id="e729f-113">指定要測試的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="e729f-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="e729f-114">您必須包含下列字串：</span><span class="sxs-lookup"><span data-stu-id="e729f-114">You must include the following string:</span></span> 

<span data-ttu-id="e729f-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="e729f-115">.trafficmanager.net</span></span>

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

### <span data-ttu-id="e729f-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e729f-116">-Profile</span></span>
<span data-ttu-id="e729f-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e729f-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e729f-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e729f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e729f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e729f-119">CommonParameters</span></span>
<span data-ttu-id="e729f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e729f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e729f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e729f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e729f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e729f-122">INPUTS</span></span>

## <span data-ttu-id="e729f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e729f-123">OUTPUTS</span></span>

### <span data-ttu-id="e729f-124">System.object</span><span class="sxs-lookup"><span data-stu-id="e729f-124">System.Boolean</span></span>
<span data-ttu-id="e729f-125">這個 Cmdlet 會產生 $True 或 $False。</span><span class="sxs-lookup"><span data-stu-id="e729f-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="e729f-126">如果有可用的功能變數名稱，這個 Cmdlet 會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="e729f-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="e729f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e729f-127">NOTES</span></span>

## <span data-ttu-id="e729f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e729f-128">RELATED LINKS</span></span>

