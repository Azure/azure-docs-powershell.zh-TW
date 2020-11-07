---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966993"
---
# <span data-ttu-id="154f9-101">Get-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="154f9-101">Get-AzureStoreAddOn</span></span>

## <span data-ttu-id="154f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="154f9-102">SYNOPSIS</span></span>
<span data-ttu-id="154f9-103">取得可用的 Azure 書店附加元件。</span><span class="sxs-lookup"><span data-stu-id="154f9-103">Gets the available Azure Store add-ons.</span></span>

## <span data-ttu-id="154f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="154f9-104">SYNTAX</span></span>

### <span data-ttu-id="154f9-105">ListAvailable</span><span class="sxs-lookup"><span data-stu-id="154f9-105">ListAvailable</span></span>
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="154f9-106">GetAddOn</span><span class="sxs-lookup"><span data-stu-id="154f9-106">GetAddOn</span></span>
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="154f9-107">說明</span><span class="sxs-lookup"><span data-stu-id="154f9-107">DESCRIPTION</span></span>
<span data-ttu-id="154f9-108">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="154f9-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="154f9-109">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="154f9-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="154f9-110">從 Azure 書店取得購買的所有可用附加元件，或取得目前訂閱的現有附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="154f9-110">Gets all the available add-ons for purchasing from the Azure Store, or gets the existing add-on instances for the current subscription.</span></span>

## <span data-ttu-id="154f9-111">示例</span><span class="sxs-lookup"><span data-stu-id="154f9-111">EXAMPLES</span></span>

### <span data-ttu-id="154f9-112">範例1</span><span class="sxs-lookup"><span data-stu-id="154f9-112">Example 1</span></span>
```
PS C:\> Get-AzureStoreAddOn
```

<span data-ttu-id="154f9-113">這個範例會取得目前訂閱的所有購買的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="154f9-113">This example gets all purchased add-on instances for the current subscription.</span></span>

### <span data-ttu-id="154f9-114">範例2</span><span class="sxs-lookup"><span data-stu-id="154f9-114">Example 2</span></span>
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

<span data-ttu-id="154f9-115">這個範例會從 Azure 書店取得在美國購買的所有可用附加元件。</span><span class="sxs-lookup"><span data-stu-id="154f9-115">This example gets all the available add-ons for purchasing in United States from the Azure Store.</span></span>

### <span data-ttu-id="154f9-116">範例3</span><span class="sxs-lookup"><span data-stu-id="154f9-116">Example 3</span></span>
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

<span data-ttu-id="154f9-117">這個範例會從目前訂閱中購買的附加元件實例取得名為 MyAddOn 的附加元件。</span><span class="sxs-lookup"><span data-stu-id="154f9-117">This example gets an add-on named MyAddOn from the purchased add-on instance in the current subscription.</span></span>

## <span data-ttu-id="154f9-118">參數</span><span class="sxs-lookup"><span data-stu-id="154f9-118">PARAMETERS</span></span>

### <span data-ttu-id="154f9-119">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="154f9-119">-Country</span></span>
<span data-ttu-id="154f9-120">如果已指定，則只會傳回指定國家/地區內可用的 Azure Store 附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="154f9-120">If specified, returns only the Azure Store add-on instances available in the specified country.</span></span>
<span data-ttu-id="154f9-121">預設值為 "US"。</span><span class="sxs-lookup"><span data-stu-id="154f9-121">The default is "US".</span></span>

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154f9-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="154f9-122">-ListAvailable</span></span>
<span data-ttu-id="154f9-123">如果已指定，就會從 Azure 存放區取得購買的可用附加元件。</span><span class="sxs-lookup"><span data-stu-id="154f9-123">If specified, gets available add-ons for purchasing from the Azure Store.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154f9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="154f9-124">-Name</span></span>
<span data-ttu-id="154f9-125">傳回符合指定名稱的附加元件。</span><span class="sxs-lookup"><span data-stu-id="154f9-125">Returns the add-on that matches the specified name.</span></span>

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="154f9-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="154f9-126">-Profile</span></span>
<span data-ttu-id="154f9-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="154f9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="154f9-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="154f9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="154f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154f9-129">CommonParameters</span></span>
<span data-ttu-id="154f9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="154f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154f9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="154f9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154f9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="154f9-132">INPUTS</span></span>

## <span data-ttu-id="154f9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="154f9-133">OUTPUTS</span></span>

## <span data-ttu-id="154f9-134">筆記</span><span class="sxs-lookup"><span data-stu-id="154f9-134">NOTES</span></span>

## <span data-ttu-id="154f9-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="154f9-135">RELATED LINKS</span></span>

[<span data-ttu-id="154f9-136">新-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="154f9-136">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="154f9-137">移除-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="154f9-137">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="154f9-138">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="154f9-138">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


