---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: ea159b52de0dd7d30c898f5119bc819c94d418fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905553"
---
# <span data-ttu-id="011a0-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="011a0-101">Set-AzDataShare</span></span>

## <span data-ttu-id="011a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="011a0-102">SYNOPSIS</span></span>
<span data-ttu-id="011a0-103">更新現有的資料共用</span><span class="sxs-lookup"><span data-stu-id="011a0-103">Updates an existing data share</span></span>

## <span data-ttu-id="011a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="011a0-104">SYNTAX</span></span>

### <span data-ttu-id="011a0-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="011a0-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="011a0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="011a0-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="011a0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="011a0-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="011a0-108">描述</span><span class="sxs-lookup"><span data-stu-id="011a0-108">DESCRIPTION</span></span>
<span data-ttu-id="011a0-109">**Set-AzDataShare** Cmdlet 會更新特定 Azure 資料共用帳戶內的資料共用。</span><span class="sxs-lookup"><span data-stu-id="011a0-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="011a0-110">例子</span><span class="sxs-lookup"><span data-stu-id="011a0-110">EXAMPLES</span></span>

### <span data-ttu-id="011a0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="011a0-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="011a0-112">此命令會更新名為 AdsShare 的現有資料共用</span><span class="sxs-lookup"><span data-stu-id="011a0-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="011a0-113">參數</span><span class="sxs-lookup"><span data-stu-id="011a0-113">PARAMETERS</span></span>

### <span data-ttu-id="011a0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="011a0-114">-AccountName</span></span>
<span data-ttu-id="011a0-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="011a0-115">Azure data share account name</span></span>

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

### <span data-ttu-id="011a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011a0-116">-DefaultProfile</span></span>
<span data-ttu-id="011a0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="011a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="011a0-118">-描述</span><span class="sxs-lookup"><span data-stu-id="011a0-118">-Description</span></span>
<span data-ttu-id="011a0-119">資料共用的描述</span><span class="sxs-lookup"><span data-stu-id="011a0-119">Description of Data Share</span></span>

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

### <span data-ttu-id="011a0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="011a0-120">-InputObject</span></span>
<span data-ttu-id="011a0-121">Azure 資料共用物件</span><span class="sxs-lookup"><span data-stu-id="011a0-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="011a0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="011a0-122">-Name</span></span>
<span data-ttu-id="011a0-123">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="011a0-123">Azure data share name</span></span>

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

### <span data-ttu-id="011a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="011a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="011a0-125">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="011a0-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="011a0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="011a0-126">-ResourceId</span></span>
<span data-ttu-id="011a0-127">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="011a0-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="011a0-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="011a0-128">-TermsOfUse</span></span>
<span data-ttu-id="011a0-129">資料共用使用條款</span><span class="sxs-lookup"><span data-stu-id="011a0-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="011a0-130">-確認</span><span class="sxs-lookup"><span data-stu-id="011a0-130">-Confirm</span></span>
<span data-ttu-id="011a0-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="011a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="011a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="011a0-132">-WhatIf</span></span>
<span data-ttu-id="011a0-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="011a0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="011a0-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="011a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="011a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011a0-135">CommonParameters</span></span>
<span data-ttu-id="011a0-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="011a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011a0-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="011a0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011a0-138">輸入</span><span class="sxs-lookup"><span data-stu-id="011a0-138">INPUTS</span></span>

### <span data-ttu-id="011a0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="011a0-139">System.String</span></span>

### <span data-ttu-id="011a0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="011a0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="011a0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="011a0-141">OUTPUTS</span></span>

### <span data-ttu-id="011a0-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="011a0-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="011a0-143">筆記</span><span class="sxs-lookup"><span data-stu-id="011a0-143">NOTES</span></span>

## <span data-ttu-id="011a0-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="011a0-144">RELATED LINKS</span></span>
