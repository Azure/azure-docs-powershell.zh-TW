---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F5EC8E00-E504-436A-96FF-4E886579AEA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b72fcfac0b000a8fcfc11dbab6961460cb25b8b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967861"
---
# <span data-ttu-id="d0507-101">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d0507-101">Set-AzureStoreAddOn</span></span>

## <span data-ttu-id="d0507-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0507-102">SYNOPSIS</span></span>
<span data-ttu-id="d0507-103">更新現有的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="d0507-103">Updates an existing add-on instance.</span></span>

## <span data-ttu-id="d0507-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0507-104">SYNTAX</span></span>

```
Set-AzureStoreAddOn -Name <String> -Plan <String> [-PromotionCode <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d0507-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0507-105">DESCRIPTION</span></span>
<span data-ttu-id="d0507-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0507-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d0507-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="d0507-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d0507-108">這個 Cmdlet 會從目前的訂閱更新現有的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="d0507-108">This cmdlet updates an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="d0507-109">示例</span><span class="sxs-lookup"><span data-stu-id="d0507-109">EXAMPLES</span></span>

### <span data-ttu-id="d0507-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d0507-110">Example 1</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId
```

<span data-ttu-id="d0507-111">這個範例會使用新的方案識別碼來更新附加元件。</span><span class="sxs-lookup"><span data-stu-id="d0507-111">This example updates an add-on with a new plan ID.</span></span>

### <span data-ttu-id="d0507-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d0507-112">Example 2</span></span>
```
PS C:\> Set-AzureStoreAddOn MyAddOn NewPlanId MyPromoCode
```

<span data-ttu-id="d0507-113">這個範例會使用新的方案識別碼及促銷代碼更新附加元件。</span><span class="sxs-lookup"><span data-stu-id="d0507-113">This example updates an add-on with a new plan ID and promotional code.</span></span>

## <span data-ttu-id="d0507-114">參數</span><span class="sxs-lookup"><span data-stu-id="d0507-114">PARAMETERS</span></span>

### <span data-ttu-id="d0507-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0507-115">-Name</span></span>
<span data-ttu-id="d0507-116">指定附加元件實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0507-116">Specifies the name of the add-on instance.</span></span>

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

### <span data-ttu-id="d0507-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0507-117">-PassThru</span></span>
<span data-ttu-id="d0507-118">如果已指定，則如果命令成功，則 Cmdlet 會傳回 true，否則會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="d0507-118">If specified, the cmdlet returns true if the command succeeds and false if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0507-119">-方案</span><span class="sxs-lookup"><span data-stu-id="d0507-119">-Plan</span></span>
<span data-ttu-id="d0507-120">指定 [方案識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d0507-120">Specifies the plan ID.</span></span>

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

### <span data-ttu-id="d0507-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d0507-121">-Profile</span></span>
<span data-ttu-id="d0507-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d0507-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d0507-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d0507-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0507-124">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="d0507-124">-PromotionCode</span></span>
<span data-ttu-id="d0507-125">指定促銷代碼。</span><span class="sxs-lookup"><span data-stu-id="d0507-125">Specifies the promotional code.</span></span>

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

### <span data-ttu-id="d0507-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0507-126">CommonParameters</span></span>
<span data-ttu-id="d0507-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0507-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0507-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0507-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0507-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d0507-129">INPUTS</span></span>

## <span data-ttu-id="d0507-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d0507-130">OUTPUTS</span></span>

## <span data-ttu-id="d0507-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d0507-131">NOTES</span></span>

## <span data-ttu-id="d0507-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0507-132">RELATED LINKS</span></span>

[<span data-ttu-id="d0507-133">AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d0507-133">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="d0507-134">新-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d0507-134">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="d0507-135">移除-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="d0507-135">Remove-AzureStoreAddOn</span></span>](./Remove-AzureStoreAddOn.md)


