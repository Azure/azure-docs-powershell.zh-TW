---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966894"
---
# <span data-ttu-id="73b53-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="73b53-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="73b53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73b53-102">SYNOPSIS</span></span>
<span data-ttu-id="73b53-103">將資源設定為目前的資源。</span><span class="sxs-lookup"><span data-stu-id="73b53-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="73b53-104">句法</span><span class="sxs-lookup"><span data-stu-id="73b53-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="73b53-105">說明</span><span class="sxs-lookup"><span data-stu-id="73b53-105">DESCRIPTION</span></span>
<span data-ttu-id="73b53-106">**AzureStorSimpleResource** Cmdlet 會將資源設定為目前的資源。</span><span class="sxs-lookup"><span data-stu-id="73b53-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="73b53-107">選取資源之後，其他 Cmdlet 會套用在該資源內容中。</span><span class="sxs-lookup"><span data-stu-id="73b53-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="73b53-108">示例</span><span class="sxs-lookup"><span data-stu-id="73b53-108">EXAMPLES</span></span>

### <span data-ttu-id="73b53-109">範例1：第一次選取資源</span><span class="sxs-lookup"><span data-stu-id="73b53-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="73b53-110">這個命令會選取名為 Contoso64-Tsqa 的資源作為目前的內容。</span><span class="sxs-lookup"><span data-stu-id="73b53-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="73b53-111">在這個範例中，電腦先前沒有初始化此內容，因此您必須指定 *RegistrationKey* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="73b53-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="73b53-112">範例2：嘗試選取資源</span><span class="sxs-lookup"><span data-stu-id="73b53-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="73b53-113">範例3：選取先前選取的資源</span><span class="sxs-lookup"><span data-stu-id="73b53-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="73b53-114">這個命令會選取名為 Contoso64-Tsqa 的資源作為目前的內容。</span><span class="sxs-lookup"><span data-stu-id="73b53-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="73b53-115">在這個範例中，先前已選取該內容，因此您不需要指定 *RegistrationKey* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="73b53-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="73b53-116">參數</span><span class="sxs-lookup"><span data-stu-id="73b53-116">PARAMETERS</span></span>

### <span data-ttu-id="73b53-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="73b53-117">-Profile</span></span>
<span data-ttu-id="73b53-118">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="73b53-118">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="73b53-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="73b53-119">-RegistrationKey</span></span>
<span data-ttu-id="73b53-120">指定註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="73b53-120">Specifies a registration key.</span></span>
<span data-ttu-id="73b53-121">第一次選取資源時，請指定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="73b53-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="73b53-122">在這個 Cmdlet 選取目前的資源之後，Cmdlet 會根據需要使用此金鑰。</span><span class="sxs-lookup"><span data-stu-id="73b53-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="73b53-123">如需詳細資訊，請參閱取得 Microsoft 開發人員網路上 [的服務註冊金鑰](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="73b53-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

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

### <span data-ttu-id="73b53-124">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="73b53-124">-ResourceName</span></span>
<span data-ttu-id="73b53-125">指定要選取為目前資源之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="73b53-125">Specifies the name of the resource to select as the current resource.</span></span>

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

### <span data-ttu-id="73b53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b53-126">CommonParameters</span></span>
<span data-ttu-id="73b53-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73b53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b53-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73b53-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b53-129">輸入</span><span class="sxs-lookup"><span data-stu-id="73b53-129">INPUTS</span></span>

### <span data-ttu-id="73b53-130">所有</span><span class="sxs-lookup"><span data-stu-id="73b53-130">None</span></span>

## <span data-ttu-id="73b53-131">輸出</span><span class="sxs-lookup"><span data-stu-id="73b53-131">OUTPUTS</span></span>

### <span data-ttu-id="73b53-132">StorSimpleResourceCoNtext</span><span class="sxs-lookup"><span data-stu-id="73b53-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="73b53-133">這個 Cmdlet 會傳回 **StorSimpleResourceCoNtext** 物件，其中包含資源內容的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="73b53-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="73b53-134">筆記</span><span class="sxs-lookup"><span data-stu-id="73b53-134">NOTES</span></span>

## <span data-ttu-id="73b53-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="73b53-135">RELATED LINKS</span></span>

[<span data-ttu-id="73b53-136">AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="73b53-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="73b53-137">AzureStorSimpleResourceCoNtext</span><span class="sxs-lookup"><span data-stu-id="73b53-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)


