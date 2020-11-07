---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967995"
---
# <span data-ttu-id="9a687-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="9a687-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="9a687-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a687-102">SYNOPSIS</span></span>
<span data-ttu-id="9a687-103">取得目前的資源內容。</span><span class="sxs-lookup"><span data-stu-id="9a687-103">Gets the current resource context.</span></span>

## <span data-ttu-id="9a687-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a687-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9a687-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a687-105">DESCRIPTION</span></span>
<span data-ttu-id="9a687-106">**AzureStorSimpleResourceCoNtext** Cmdlet 會取得目前的資源內容。</span><span class="sxs-lookup"><span data-stu-id="9a687-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="9a687-107">示例</span><span class="sxs-lookup"><span data-stu-id="9a687-107">EXAMPLES</span></span>

### <span data-ttu-id="9a687-108">範例1：取得目前的內容</span><span class="sxs-lookup"><span data-stu-id="9a687-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="9a687-109">第一個命令會使用 **AzureStorSimpleResource** Cmdlet，將目前的內容設為名為 Contoso63-Tsqa 的資源。</span><span class="sxs-lookup"><span data-stu-id="9a687-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="9a687-110">第二個命令會取得目前的資源內容。</span><span class="sxs-lookup"><span data-stu-id="9a687-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="9a687-111">範例2：嘗試取得目前的內容</span><span class="sxs-lookup"><span data-stu-id="9a687-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="9a687-112">這個命令會取得目前的內容。</span><span class="sxs-lookup"><span data-stu-id="9a687-112">This command gets the current context.</span></span>
<span data-ttu-id="9a687-113">在這個範例中，沒有設定任何內容。</span><span class="sxs-lookup"><span data-stu-id="9a687-113">In this example, no context has been set.</span></span>
<span data-ttu-id="9a687-114">命令會傳回說明問題的訊息。</span><span class="sxs-lookup"><span data-stu-id="9a687-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="9a687-115">參數</span><span class="sxs-lookup"><span data-stu-id="9a687-115">PARAMETERS</span></span>

### <span data-ttu-id="9a687-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9a687-116">-Profile</span></span>
<span data-ttu-id="9a687-117">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9a687-117">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9a687-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a687-118">CommonParameters</span></span>
<span data-ttu-id="9a687-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a687-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a687-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a687-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a687-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9a687-121">INPUTS</span></span>

### <span data-ttu-id="9a687-122">所有</span><span class="sxs-lookup"><span data-stu-id="9a687-122">None</span></span>

## <span data-ttu-id="9a687-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9a687-123">OUTPUTS</span></span>

### <span data-ttu-id="9a687-124">StorSimpleResourceCoNtext</span><span class="sxs-lookup"><span data-stu-id="9a687-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="9a687-125">這個 Cmdlet 會傳回 **ResourceCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="9a687-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="9a687-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9a687-126">NOTES</span></span>

## <span data-ttu-id="9a687-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a687-127">RELATED LINKS</span></span>

[<span data-ttu-id="9a687-128">AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="9a687-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="9a687-129">選取-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="9a687-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


