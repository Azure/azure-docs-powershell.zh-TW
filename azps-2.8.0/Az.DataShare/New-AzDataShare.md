---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: ccb40de9ef5e9e68cf62b7b05edeaac9ae10efbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612658"
---
# <span data-ttu-id="2586f-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="2586f-101">New-AzDataShare</span></span>

## <span data-ttu-id="2586f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2586f-102">SYNOPSIS</span></span>
<span data-ttu-id="2586f-103">建立 azure 資料共用。</span><span class="sxs-lookup"><span data-stu-id="2586f-103">Creates a azure data share.</span></span>

## <span data-ttu-id="2586f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2586f-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2586f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2586f-105">DESCRIPTION</span></span>
<span data-ttu-id="2586f-106">**新的-AzDataShare** Cmdlet 會提供資源群組名稱、帳戶名稱、共用名稱稱和共用類型，在指定的 azure 資料共用帳戶內建立資料共用。</span><span class="sxs-lookup"><span data-stu-id="2586f-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="2586f-107">[描述] 和 [使用條款] 是可在建立資料共用時設定的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="2586f-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="2586f-108">示例</span><span class="sxs-lookup"><span data-stu-id="2586f-108">EXAMPLES</span></span>

### <span data-ttu-id="2586f-109">範例1：建立資料共用</span><span class="sxs-lookup"><span data-stu-id="2586f-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="2586f-110">這個命令會在 [資料共用帳戶] WikiAdsAccount 中建立名為 CopyBased 的資料共用，並在 [資源群組廣告] 底下，使用 [描述] 和 [使用條款]。</span><span class="sxs-lookup"><span data-stu-id="2586f-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="2586f-111">參數</span><span class="sxs-lookup"><span data-stu-id="2586f-111">PARAMETERS</span></span>

### <span data-ttu-id="2586f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2586f-112">-AccountName</span></span>
<span data-ttu-id="2586f-113">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="2586f-113">Azure data share account name</span></span>

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

### <span data-ttu-id="2586f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2586f-114">-DefaultProfile</span></span>
<span data-ttu-id="2586f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2586f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2586f-116">-描述</span><span class="sxs-lookup"><span data-stu-id="2586f-116">-Description</span></span>
<span data-ttu-id="2586f-117">Azure 資料共用的描述</span><span class="sxs-lookup"><span data-stu-id="2586f-117">Description of azure data share</span></span>

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

### <span data-ttu-id="2586f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2586f-118">-Name</span></span>
<span data-ttu-id="2586f-119">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="2586f-119">Azure data share name</span></span>

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

### <span data-ttu-id="2586f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2586f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2586f-121">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="2586f-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2586f-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="2586f-122">-TermsOfUse</span></span>
<span data-ttu-id="2586f-123">Azure data share 的使用條款</span><span class="sxs-lookup"><span data-stu-id="2586f-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="2586f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2586f-124">-Confirm</span></span>
<span data-ttu-id="2586f-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2586f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2586f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2586f-126">-WhatIf</span></span>
<span data-ttu-id="2586f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2586f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2586f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2586f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2586f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2586f-129">CommonParameters</span></span>
<span data-ttu-id="2586f-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2586f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2586f-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2586f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2586f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2586f-132">INPUTS</span></span>

### <span data-ttu-id="2586f-133">所有</span><span class="sxs-lookup"><span data-stu-id="2586f-133">None</span></span>

## <span data-ttu-id="2586f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2586f-134">OUTPUTS</span></span>

### <span data-ttu-id="2586f-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="2586f-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="2586f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2586f-136">NOTES</span></span>

## <span data-ttu-id="2586f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2586f-137">RELATED LINKS</span></span>
