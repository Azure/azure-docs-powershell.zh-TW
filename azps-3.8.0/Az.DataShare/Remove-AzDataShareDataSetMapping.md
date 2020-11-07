---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 3e28b55a77ffb5f8d4ba95743e897628948d15f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958812"
---
# <span data-ttu-id="754a4-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="754a4-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="754a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="754a4-102">SYNOPSIS</span></span>
<span data-ttu-id="754a4-103">移除資料集對應</span><span class="sxs-lookup"><span data-stu-id="754a4-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="754a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="754a4-104">SYNTAX</span></span>

### <span data-ttu-id="754a4-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="754a4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754a4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="754a4-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754a4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="754a4-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="754a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="754a4-108">DESCRIPTION</span></span>
<span data-ttu-id="754a4-109">**AzDataShareDataSetMapping** Cmdlet 會移除資料集對應。</span><span class="sxs-lookup"><span data-stu-id="754a4-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="754a4-110">示例</span><span class="sxs-lookup"><span data-stu-id="754a4-110">EXAMPLES</span></span>

### <span data-ttu-id="754a4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="754a4-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="754a4-112">這個命令會從 sharesubscription WikiAds 中移除名為 DSM 的資料集。</span><span class="sxs-lookup"><span data-stu-id="754a4-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="754a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="754a4-113">PARAMETERS</span></span>

### <span data-ttu-id="754a4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="754a4-114">-AccountName</span></span>
<span data-ttu-id="754a4-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="754a4-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="754a4-116">-DefaultProfile</span></span>
<span data-ttu-id="754a4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="754a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="754a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="754a4-118">-InputObject</span></span>
<span data-ttu-id="754a4-119">Azure 資料集對應物件</span><span class="sxs-lookup"><span data-stu-id="754a4-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="754a4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="754a4-120">-Name</span></span>
<span data-ttu-id="754a4-121">Azure 資料集對應名稱</span><span class="sxs-lookup"><span data-stu-id="754a4-121">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="754a4-122">-PassThru</span></span>
<span data-ttu-id="754a4-123">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="754a4-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="754a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="754a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="754a4-125">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="754a4-125">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="754a4-126">-ResourceId</span></span>
<span data-ttu-id="754a4-127">Azure 資料集對應的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="754a4-127">The resource id of the azure data set mapping</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="754a4-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="754a4-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="754a4-129">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="754a4-129">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754a4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="754a4-130">-Confirm</span></span>
<span data-ttu-id="754a4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="754a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="754a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="754a4-132">-WhatIf</span></span>
<span data-ttu-id="754a4-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="754a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="754a4-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="754a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="754a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754a4-135">CommonParameters</span></span>
<span data-ttu-id="754a4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="754a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754a4-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="754a4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754a4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="754a4-138">INPUTS</span></span>

### <span data-ttu-id="754a4-139">System.object</span><span class="sxs-lookup"><span data-stu-id="754a4-139">System.String</span></span>

### <span data-ttu-id="754a4-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="754a4-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="754a4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="754a4-141">OUTPUTS</span></span>

### <span data-ttu-id="754a4-142">System.object</span><span class="sxs-lookup"><span data-stu-id="754a4-142">System.Boolean</span></span>

## <span data-ttu-id="754a4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="754a4-143">NOTES</span></span>

## <span data-ttu-id="754a4-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="754a4-144">RELATED LINKS</span></span>
