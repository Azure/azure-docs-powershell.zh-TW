---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967958"
---
# <span data-ttu-id="f70f6-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="f70f6-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="f70f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f70f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f70f6-103">在目前的訂閱中取得 Azure web 託管方案。</span><span class="sxs-lookup"><span data-stu-id="f70f6-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="f70f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="f70f6-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f70f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="f70f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f70f6-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f70f6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f70f6-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="f70f6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f70f6-108">**AzureWebHostingPlan** Cmdlet 會在目前的訂閱中取得 Azure web 託管方案。</span><span class="sxs-lookup"><span data-stu-id="f70f6-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="f70f6-109">根據預設， **AzureWebHostingPlan** 會取得目前訂閱中的所有 Azure 託管方案，並傳回提供方案基本資訊的物件。</span><span class="sxs-lookup"><span data-stu-id="f70f6-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="f70f6-110">當您使用 *Web 空間* 和 *名稱* 參數時， **AzureWebHostingPlan** 會傳回特定的託管方案物件。</span><span class="sxs-lookup"><span data-stu-id="f70f6-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="f70f6-111">若要尋找目前的訂閱，請使用 **AzureSubscription** Cmdlet 的 *目前* 參數。</span><span class="sxs-lookup"><span data-stu-id="f70f6-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="f70f6-112">若要變更目前的訂閱，請使用 **AzureSubscription** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f70f6-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="f70f6-113">示例</span><span class="sxs-lookup"><span data-stu-id="f70f6-113">EXAMPLES</span></span>

### <span data-ttu-id="f70f6-114">範例1：取得訂閱中的所有 web 主機託管方案</span><span class="sxs-lookup"><span data-stu-id="f70f6-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="f70f6-115">這個命令會在目前的訂閱中取得所有的 Azure web 主機託管方案。</span><span class="sxs-lookup"><span data-stu-id="f70f6-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="f70f6-116">範例2：在訂閱中取得特定的 web 主機託管方案</span><span class="sxs-lookup"><span data-stu-id="f70f6-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="f70f6-117">這個命令會在目前訂閱中名為 westeuropewebspace 的 web 空間中，取得名為 Default0 的 web 託管方案。</span><span class="sxs-lookup"><span data-stu-id="f70f6-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="f70f6-118">參數</span><span class="sxs-lookup"><span data-stu-id="f70f6-118">PARAMETERS</span></span>

### <span data-ttu-id="f70f6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f70f6-119">-Name</span></span>
<span data-ttu-id="f70f6-120">指定訂閱中的方案名稱。</span><span class="sxs-lookup"><span data-stu-id="f70f6-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="f70f6-121">根據預設，此 Cmdlet 會取得目前訂閱中的所有方案。</span><span class="sxs-lookup"><span data-stu-id="f70f6-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="f70f6-122">這個參數不支援萬用字元字元。</span><span class="sxs-lookup"><span data-stu-id="f70f6-122">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="f70f6-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f70f6-123">-Profile</span></span>
<span data-ttu-id="f70f6-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f70f6-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f70f6-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f70f6-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f70f6-126">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="f70f6-126">-WebSpaceName</span></span>
<span data-ttu-id="f70f6-127">指定訂閱中的 web 空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f70f6-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="f70f6-128">根據預設，此 Cmdlet 會取得指定 web 空間中的所有網站。</span><span class="sxs-lookup"><span data-stu-id="f70f6-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="f70f6-129">這個參數不支援萬用字元字元。</span><span class="sxs-lookup"><span data-stu-id="f70f6-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70f6-130">CommonParameters</span></span>
<span data-ttu-id="f70f6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f70f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70f6-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f70f6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70f6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f70f6-133">INPUTS</span></span>

###  
<span data-ttu-id="f70f6-134">您可以透過屬性名稱（而不是依值），將輸入傳遞到此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f70f6-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f70f6-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f70f6-135">OUTPUTS</span></span>

### <span data-ttu-id="f70f6-136">WindowsAzure. WebEntities. WebHostingPlan （）</span><span class="sxs-lookup"><span data-stu-id="f70f6-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="f70f6-137">根據預設， **AzureWebHostingPlan** 會傳回 **WebHostingPlan** 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="f70f6-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="f70f6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f70f6-138">NOTES</span></span>

## <span data-ttu-id="f70f6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f70f6-139">RELATED LINKS</span></span>

