---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967000"
---
# <span data-ttu-id="e242d-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="e242d-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="e242d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e242d-102">SYNOPSIS</span></span>
<span data-ttu-id="e242d-103">取得您建立的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="e242d-104">句法</span><span class="sxs-lookup"><span data-stu-id="e242d-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e242d-105">說明</span><span class="sxs-lookup"><span data-stu-id="e242d-105">DESCRIPTION</span></span>
<span data-ttu-id="e242d-106">**AzureStorSimpleResource** Cmdlet 會取得您使用 Azure 入口網站建立的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="e242d-107">Cmdlet 會取得您可以用來連線至資源的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e242d-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="e242d-108">示例</span><span class="sxs-lookup"><span data-stu-id="e242d-108">EXAMPLES</span></span>

### <span data-ttu-id="e242d-109">範例1：取得所有資源</span><span class="sxs-lookup"><span data-stu-id="e242d-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="e242d-110">這個命令會取得您建立的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="e242d-111">在這個範例中，有三個資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="e242d-112">範例2：使用名稱取得資源</span><span class="sxs-lookup"><span data-stu-id="e242d-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="e242d-113">這個命令會取得名為 Contoso63-Tsqa 的資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="e242d-114">範例3：嘗試取得不存在的資源</span><span class="sxs-lookup"><span data-stu-id="e242d-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="e242d-115">這個命令會嘗試取得名為 Contoso64-Tsqa 的資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="e242d-116">沒有擁有此名稱的資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-116">There is no resource that has this name.</span></span>
<span data-ttu-id="e242d-117">這個範例不會傳回任何資源。</span><span class="sxs-lookup"><span data-stu-id="e242d-117">This example does not return any resource.</span></span>

## <span data-ttu-id="e242d-118">參數</span><span class="sxs-lookup"><span data-stu-id="e242d-118">PARAMETERS</span></span>

### <span data-ttu-id="e242d-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e242d-119">-Profile</span></span>
<span data-ttu-id="e242d-120">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e242d-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e242d-121">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="e242d-121">-ResourceName</span></span>
<span data-ttu-id="e242d-122">指定此 Cmdlet 所取得之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e242d-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e242d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e242d-123">CommonParameters</span></span>
<span data-ttu-id="e242d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e242d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e242d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e242d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e242d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e242d-126">INPUTS</span></span>

### <span data-ttu-id="e242d-127">所有</span><span class="sxs-lookup"><span data-stu-id="e242d-127">None</span></span>

## <span data-ttu-id="e242d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e242d-128">OUTPUTS</span></span>

### <span data-ttu-id="e242d-129">IEnumerable \<ResourceCredentials\> 、ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="e242d-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="e242d-130">這個 Cmdlet 會傳回包含下列屬性的 **ResourceCredentials** 物件：</span><span class="sxs-lookup"><span data-stu-id="e242d-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="e242d-131">**CoNtext.resourcename**</span><span class="sxs-lookup"><span data-stu-id="e242d-131">**ResourceName**</span></span>
- <span data-ttu-id="e242d-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="e242d-132">**ResouceId**</span></span>
- <span data-ttu-id="e242d-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="e242d-133">**ResourceState**</span></span>

## <span data-ttu-id="e242d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e242d-134">NOTES</span></span>

## <span data-ttu-id="e242d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e242d-135">RELATED LINKS</span></span>

[<span data-ttu-id="e242d-136">AzureStorSimpleResourceCoNtext</span><span class="sxs-lookup"><span data-stu-id="e242d-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="e242d-137">選取-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="e242d-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


