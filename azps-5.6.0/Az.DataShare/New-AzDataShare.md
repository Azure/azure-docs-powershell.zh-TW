---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: cda809b8c6c4425a3df7bd4ba5ae40a9292e358f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914009"
---
# <span data-ttu-id="7517b-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="7517b-101">New-AzDataShare</span></span>

## <span data-ttu-id="7517b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7517b-102">SYNOPSIS</span></span>
<span data-ttu-id="7517b-103">建立 Azure 資料共用。</span><span class="sxs-lookup"><span data-stu-id="7517b-103">Creates a azure data share.</span></span>

## <span data-ttu-id="7517b-104">語法</span><span class="sxs-lookup"><span data-stu-id="7517b-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7517b-105">描述</span><span class="sxs-lookup"><span data-stu-id="7517b-105">DESCRIPTION</span></span>
<span data-ttu-id="7517b-106">**New-AzDataShare** Cmdlet 會提供資源組名、帳戶名稱、共用名稱稱和共用類型，以在指定的 Azure 資料共用帳戶中建立資料共用。</span><span class="sxs-lookup"><span data-stu-id="7517b-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="7517b-107">描述和使用規定是可于建立資料共用時可設定之選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="7517b-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="7517b-108">例子</span><span class="sxs-lookup"><span data-stu-id="7517b-108">EXAMPLES</span></span>

### <span data-ttu-id="7517b-109">範例 1：建立資料共用</span><span class="sxs-lookup"><span data-stu-id="7517b-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="7517b-110">此命令在資源群組 ADS 下建立名為 AdsShare 的資料類型 CopyBased 資料共用帳戶 WikiAdsAccount，並包含描述和使用規定。</span><span class="sxs-lookup"><span data-stu-id="7517b-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="7517b-111">參數</span><span class="sxs-lookup"><span data-stu-id="7517b-111">PARAMETERS</span></span>

### <span data-ttu-id="7517b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7517b-112">-AccountName</span></span>
<span data-ttu-id="7517b-113">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="7517b-113">Azure data share account name</span></span>

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

### <span data-ttu-id="7517b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7517b-114">-DefaultProfile</span></span>
<span data-ttu-id="7517b-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7517b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7517b-116">-描述</span><span class="sxs-lookup"><span data-stu-id="7517b-116">-Description</span></span>
<span data-ttu-id="7517b-117">Azure 資料共用的描述</span><span class="sxs-lookup"><span data-stu-id="7517b-117">Description of azure data share</span></span>

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

### <span data-ttu-id="7517b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7517b-118">-Name</span></span>
<span data-ttu-id="7517b-119">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="7517b-119">Azure data share name</span></span>

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

### <span data-ttu-id="7517b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7517b-120">-ResourceGroupName</span></span>
<span data-ttu-id="7517b-121">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="7517b-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7517b-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="7517b-122">-TermsOfUse</span></span>
<span data-ttu-id="7517b-123">Azure 資料共用使用條款</span><span class="sxs-lookup"><span data-stu-id="7517b-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="7517b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7517b-124">-Confirm</span></span>
<span data-ttu-id="7517b-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7517b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7517b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7517b-126">-WhatIf</span></span>
<span data-ttu-id="7517b-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7517b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7517b-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7517b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7517b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7517b-129">CommonParameters</span></span>
<span data-ttu-id="7517b-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7517b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7517b-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7517b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7517b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7517b-132">INPUTS</span></span>

### <span data-ttu-id="7517b-133">沒有</span><span class="sxs-lookup"><span data-stu-id="7517b-133">None</span></span>

## <span data-ttu-id="7517b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7517b-134">OUTPUTS</span></span>

### <span data-ttu-id="7517b-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="7517b-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="7517b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7517b-136">NOTES</span></span>

## <span data-ttu-id="7517b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7517b-137">RELATED LINKS</span></span>
