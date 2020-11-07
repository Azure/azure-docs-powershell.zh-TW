---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967775"
---
# <span data-ttu-id="486ae-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="486ae-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="486ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="486ae-102">SYNOPSIS</span></span>
<span data-ttu-id="486ae-103">檢索 Azure RemoteApp 集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="486ae-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="486ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="486ae-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="486ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="486ae-105">DESCRIPTION</span></span>
<span data-ttu-id="486ae-106">**AzureRemoteAppCollection** Cmdlet 會在 Microsoft Azure 中檢索 Azure RemoteApp 集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="486ae-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="486ae-107">它會傳回包含特定集合之資訊的物件，或者如果沒有指定集合，則會傳回目前訂閱中所有集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="486ae-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="486ae-108">示例</span><span class="sxs-lookup"><span data-stu-id="486ae-108">EXAMPLES</span></span>

### <span data-ttu-id="486ae-109">範例1：取得所有集合的清單</span><span class="sxs-lookup"><span data-stu-id="486ae-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="486ae-110">這個命令會傳回訂閱中所有 Azure RemoteApp 集合的清單。</span><span class="sxs-lookup"><span data-stu-id="486ae-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="486ae-111">範例2：取得指定集合的相關資訊</span><span class="sxs-lookup"><span data-stu-id="486ae-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="486ae-112">這個命令會傳回名為 ContosoApps 的 Azure RemoteApp 集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="486ae-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="486ae-113">範例3：使用萬用字元取得收藏清單</span><span class="sxs-lookup"><span data-stu-id="486ae-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="486ae-114">這個命令會傳回符合金融的所有 Azure RemoteApp 集合的清單 \*。</span><span class="sxs-lookup"><span data-stu-id="486ae-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="486ae-115">參數</span><span class="sxs-lookup"><span data-stu-id="486ae-115">PARAMETERS</span></span>

### <span data-ttu-id="486ae-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="486ae-116">-CollectionName</span></span>
<span data-ttu-id="486ae-117">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="486ae-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="486ae-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="486ae-118">-Profile</span></span>
<span data-ttu-id="486ae-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="486ae-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="486ae-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="486ae-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="486ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486ae-121">CommonParameters</span></span>
<span data-ttu-id="486ae-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="486ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486ae-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="486ae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486ae-124">輸入</span><span class="sxs-lookup"><span data-stu-id="486ae-124">INPUTS</span></span>

## <span data-ttu-id="486ae-125">輸出</span><span class="sxs-lookup"><span data-stu-id="486ae-125">OUTPUTS</span></span>

## <span data-ttu-id="486ae-126">筆記</span><span class="sxs-lookup"><span data-stu-id="486ae-126">NOTES</span></span>

## <span data-ttu-id="486ae-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="486ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="486ae-128">新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="486ae-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="486ae-129">移除-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="486ae-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="486ae-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="486ae-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="486ae-131">更新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="486ae-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


