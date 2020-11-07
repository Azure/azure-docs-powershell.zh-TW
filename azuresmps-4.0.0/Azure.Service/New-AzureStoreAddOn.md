---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 793037C4-8FE5-4799-B59B-94C1605D9F4E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 593ea36e90635472db1f8568254657f782bd1200
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967647"
---
# <span data-ttu-id="8c484-101">New-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="8c484-101">New-AzureStoreAddOn</span></span>

## <span data-ttu-id="8c484-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c484-102">SYNOPSIS</span></span>
<span data-ttu-id="8c484-103">購買新的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="8c484-103">Buys a new add-on instance.</span></span>

## <span data-ttu-id="8c484-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c484-104">SYNTAX</span></span>

```
New-AzureStoreAddOn -Name <String> -AddOn <String> -Plan <String> -Location <String> [-PromotionCode <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c484-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c484-105">DESCRIPTION</span></span>
<span data-ttu-id="8c484-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c484-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8c484-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="8c484-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8c484-108">從 Azure Store 購買新的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="8c484-108">Buys a new add-on instance from the Azure Store.</span></span>

## <span data-ttu-id="8c484-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c484-109">EXAMPLES</span></span>

### <span data-ttu-id="8c484-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8c484-110">Example 1</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US"
```

<span data-ttu-id="8c484-111">這個範例會使用 [西部美國] 位置的 PlanId 來購買名為 MyAddOn 的附加元件。</span><span class="sxs-lookup"><span data-stu-id="8c484-111">This example buys an add-on named MyAddOn with a PlanId in West US location.</span></span>

### <span data-ttu-id="8c484-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8c484-112">Example 2</span></span>
```
PS C:\> New-AzureStoreAddOn -Name MyAddOn -AddOn AddonId -Plan PlanId -Location "West US" -PromotionCode MyPromoCode
```

<span data-ttu-id="8c484-113">這個範例使用促銷程式碼來購買附加元件。</span><span class="sxs-lookup"><span data-stu-id="8c484-113">This example uses a promotional code to buy an add-on.</span></span>

## <span data-ttu-id="8c484-114">參數</span><span class="sxs-lookup"><span data-stu-id="8c484-114">PARAMETERS</span></span>

### <span data-ttu-id="8c484-115">-載入項</span><span class="sxs-lookup"><span data-stu-id="8c484-115">-AddOn</span></span>
<span data-ttu-id="8c484-116">指定附加元件 ID。</span><span class="sxs-lookup"><span data-stu-id="8c484-116">Specifies the add-on ID.</span></span>

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

### <span data-ttu-id="8c484-117">-位置</span><span class="sxs-lookup"><span data-stu-id="8c484-117">-Location</span></span>
<span data-ttu-id="8c484-118">指定附加元件的實例位置。</span><span class="sxs-lookup"><span data-stu-id="8c484-118">Specifies the add-on instance location.</span></span>

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

### <span data-ttu-id="8c484-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c484-119">-Name</span></span>
<span data-ttu-id="8c484-120">指定附加元件實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c484-120">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="8c484-121">-方案</span><span class="sxs-lookup"><span data-stu-id="8c484-121">-Plan</span></span>
<span data-ttu-id="8c484-122">指定 [方案識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8c484-122">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="8c484-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8c484-123">-Profile</span></span>
<span data-ttu-id="8c484-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c484-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c484-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8c484-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c484-126">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="8c484-126">-PromotionCode</span></span>
<span data-ttu-id="8c484-127">指定要套用至採購的促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="8c484-127">Specifies a promotion code to apply to the purchase.</span></span>

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

### <span data-ttu-id="8c484-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c484-128">CommonParameters</span></span>
<span data-ttu-id="8c484-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c484-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c484-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c484-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c484-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8c484-131">INPUTS</span></span>

## <span data-ttu-id="8c484-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8c484-132">OUTPUTS</span></span>

## <span data-ttu-id="8c484-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8c484-133">NOTES</span></span>

## <span data-ttu-id="8c484-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c484-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c484-135">AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="8c484-135">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="8c484-136">移除-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="8c484-136">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)

[<span data-ttu-id="8c484-137">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="8c484-137">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


