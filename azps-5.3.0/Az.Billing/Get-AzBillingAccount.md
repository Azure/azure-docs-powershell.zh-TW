---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450015"
---
# <span data-ttu-id="5c456-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="5c456-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="5c456-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c456-102">SYNOPSIS</span></span>
<span data-ttu-id="5c456-103">取得帳單帳戶。</span><span class="sxs-lookup"><span data-stu-id="5c456-103">Get billing accounts.</span></span>

## <span data-ttu-id="5c456-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c456-104">SYNTAX</span></span>

### <span data-ttu-id="5c456-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="5c456-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c456-106">通過</span><span class="sxs-lookup"><span data-stu-id="5c456-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c456-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c456-107">DESCRIPTION</span></span>
<span data-ttu-id="5c456-108">**AzBillingAccount** Cmdlet 會取得帳單帳戶，而使用者可以存取。</span><span class="sxs-lookup"><span data-stu-id="5c456-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="5c456-109">示例</span><span class="sxs-lookup"><span data-stu-id="5c456-109">EXAMPLES</span></span>

### <span data-ttu-id="5c456-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5c456-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="5c456-111">取得使用者有權存取的所有帳單帳戶。</span><span class="sxs-lookup"><span data-stu-id="5c456-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="5c456-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5c456-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="5c456-113">取得具有指定名稱的帳單帳戶。</span><span class="sxs-lookup"><span data-stu-id="5c456-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="5c456-114">範例3</span><span class="sxs-lookup"><span data-stu-id="5c456-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="5c456-115">取得使用者有權存取的所有帳單帳戶，並將位址包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="5c456-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="5c456-116">範例4</span><span class="sxs-lookup"><span data-stu-id="5c456-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="5c456-117">取得使用者有權存取的所有帳單帳戶，並在結果中包含帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="5c456-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="5c456-118">範例5</span><span class="sxs-lookup"><span data-stu-id="5c456-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="5c456-119">取得使用者有權存取的所有帳單帳戶，並在結果中包含帳單設定檔和發票區段。</span><span class="sxs-lookup"><span data-stu-id="5c456-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="5c456-120">範例6</span><span class="sxs-lookup"><span data-stu-id="5c456-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="5c456-121">取得具有指定名稱的帳單帳戶，然後在結果中包含 [位址]、[帳單] 設定檔和 [發票] 區段。</span><span class="sxs-lookup"><span data-stu-id="5c456-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="5c456-122">參數</span><span class="sxs-lookup"><span data-stu-id="5c456-122">PARAMETERS</span></span>

### <span data-ttu-id="5c456-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c456-123">-DefaultProfile</span></span>
<span data-ttu-id="5c456-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5c456-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c456-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="5c456-125">-IncludeAddress</span></span>
<span data-ttu-id="5c456-126">包括帳單帳戶的位址。</span><span class="sxs-lookup"><span data-stu-id="5c456-126">Include the address of the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c456-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="5c456-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="5c456-128">在帳單帳戶下包含帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="5c456-128">Include the billing profiles under the billing account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c456-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="5c456-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="5c456-130">在 [帳單帳戶] 和 [發票] 區段下方包含帳單設定檔。</span><span class="sxs-lookup"><span data-stu-id="5c456-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c456-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c456-131">-Name</span></span>
<span data-ttu-id="5c456-132">特定帳單帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c456-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c456-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="5c456-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="5c456-134">在 [計費帳戶] 底下列出帳單實體，可以用來做為建立訂閱的輸入。</span><span class="sxs-lookup"><span data-stu-id="5c456-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c456-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c456-135">CommonParameters</span></span>
<span data-ttu-id="5c456-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c456-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c456-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c456-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c456-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5c456-138">INPUTS</span></span>

### <span data-ttu-id="5c456-139">所有</span><span class="sxs-lookup"><span data-stu-id="5c456-139">None</span></span>

## <span data-ttu-id="5c456-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5c456-140">OUTPUTS</span></span>

### <span data-ttu-id="5c456-141">PSBillingAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5c456-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="5c456-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5c456-142">NOTES</span></span>

## <span data-ttu-id="5c456-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c456-143">RELATED LINKS</span></span>
