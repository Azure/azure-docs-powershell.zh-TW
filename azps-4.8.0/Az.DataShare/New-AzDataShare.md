---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129590"
---
# <span data-ttu-id="c0b7c-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="c0b7c-101">New-AzDataShare</span></span>

## <span data-ttu-id="c0b7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b7c-103">建立 azure 資料共用。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-103">Creates a azure data share.</span></span>

## <span data-ttu-id="c0b7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0b7c-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0b7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b7c-106">**新的-AzDataShare** Cmdlet 會提供資源群組名稱、帳戶名稱、共用名稱稱和共用類型，在指定的 azure 資料共用帳戶內建立資料共用。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="c0b7c-107">[描述] 和 [使用條款] 是可在建立資料共用時設定的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="c0b7c-108">示例</span><span class="sxs-lookup"><span data-stu-id="c0b7c-108">EXAMPLES</span></span>

### <span data-ttu-id="c0b7c-109">範例1：建立資料共用</span><span class="sxs-lookup"><span data-stu-id="c0b7c-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="c0b7c-110">這個命令會在 [資料共用帳戶] WikiAdsAccount 中建立名為 CopyBased 的資料共用，並在 [資源群組廣告] 底下，使用 [描述] 和 [使用條款]。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="c0b7c-111">參數</span><span class="sxs-lookup"><span data-stu-id="c0b7c-111">PARAMETERS</span></span>

### <span data-ttu-id="c0b7c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0b7c-112">-AccountName</span></span>
<span data-ttu-id="c0b7c-113">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="c0b7c-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b7c-114">-DefaultProfile</span></span>
<span data-ttu-id="c0b7c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b7c-116">-描述</span><span class="sxs-lookup"><span data-stu-id="c0b7c-116">-Description</span></span>
<span data-ttu-id="c0b7c-117">Azure 資料共用的描述</span><span class="sxs-lookup"><span data-stu-id="c0b7c-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0b7c-118">-Name</span></span>
<span data-ttu-id="c0b7c-119">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="c0b7c-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0b7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0b7c-121">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="c0b7c-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="c0b7c-122">-TermsOfUse</span></span>
<span data-ttu-id="c0b7c-123">Azure data share 的使用條款</span><span class="sxs-lookup"><span data-stu-id="c0b7c-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c0b7c-124">-Confirm</span></span>
<span data-ttu-id="c0b7c-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0b7c-126">-WhatIf</span></span>
<span data-ttu-id="c0b7c-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0b7c-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b7c-129">CommonParameters</span></span>
<span data-ttu-id="c0b7c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b7c-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0b7c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b7c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c0b7c-132">INPUTS</span></span>

### <span data-ttu-id="c0b7c-133">所有</span><span class="sxs-lookup"><span data-stu-id="c0b7c-133">None</span></span>

## <span data-ttu-id="c0b7c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c0b7c-134">OUTPUTS</span></span>

### <span data-ttu-id="c0b7c-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="c0b7c-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="c0b7c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c0b7c-136">NOTES</span></span>

## <span data-ttu-id="c0b7c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0b7c-137">RELATED LINKS</span></span>
