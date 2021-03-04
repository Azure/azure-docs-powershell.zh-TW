---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 91f6c56849d5b8ca96af2a28191cefde803f63c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910509"
---
# <span data-ttu-id="2fea7-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="2fea7-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="2fea7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2fea7-102">SYNOPSIS</span></span>
<span data-ttu-id="2fea7-103">建立新資料共用帳戶</span><span class="sxs-lookup"><span data-stu-id="2fea7-103">Creates new data share account</span></span>

## <span data-ttu-id="2fea7-104">語法</span><span class="sxs-lookup"><span data-stu-id="2fea7-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fea7-105">描述</span><span class="sxs-lookup"><span data-stu-id="2fea7-105">DESCRIPTION</span></span>
<span data-ttu-id="2fea7-106">**New-AzDataShareAccount** Cmdlet 會于指定的 Azure 資源群組中建立資料共用帳戶。</span><span class="sxs-lookup"><span data-stu-id="2fea7-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="2fea7-107">例子</span><span class="sxs-lookup"><span data-stu-id="2fea7-107">EXAMPLES</span></span>

### <span data-ttu-id="2fea7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2fea7-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="2fea7-109">在資源群組 "ADS" 中建立名為 "WikiADS" 的帳戶</span><span class="sxs-lookup"><span data-stu-id="2fea7-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="2fea7-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fea7-110">PARAMETERS</span></span>

### <span data-ttu-id="2fea7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fea7-111">-AsJob</span></span>
<span data-ttu-id="2fea7-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="2fea7-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="2fea7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fea7-113">-DefaultProfile</span></span>
<span data-ttu-id="2fea7-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2fea7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fea7-115">-位置</span><span class="sxs-lookup"><span data-stu-id="2fea7-115">-Location</span></span>
<span data-ttu-id="2fea7-116">建立資料共用帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="2fea7-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="2fea7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2fea7-117">-Name</span></span>
<span data-ttu-id="2fea7-118">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2fea7-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="2fea7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fea7-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fea7-120">Azure 資料共用帳戶的資源組名會建立于其中。</span><span class="sxs-lookup"><span data-stu-id="2fea7-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="2fea7-121">-標記</span><span class="sxs-lookup"><span data-stu-id="2fea7-121">-Tag</span></span>
<span data-ttu-id="2fea7-122">與 Azure 資料共用帳戶關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="2fea7-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fea7-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2fea7-123">-Confirm</span></span>
<span data-ttu-id="2fea7-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2fea7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fea7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fea7-125">-WhatIf</span></span>
<span data-ttu-id="2fea7-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fea7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fea7-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fea7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fea7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fea7-128">CommonParameters</span></span>
<span data-ttu-id="2fea7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2fea7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fea7-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fea7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fea7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2fea7-131">INPUTS</span></span>

### <span data-ttu-id="2fea7-132">沒有</span><span class="sxs-lookup"><span data-stu-id="2fea7-132">None</span></span>

## <span data-ttu-id="2fea7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2fea7-133">OUTPUTS</span></span>

### <span data-ttu-id="2fea7-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="2fea7-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="2fea7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2fea7-135">NOTES</span></span>

## <span data-ttu-id="2fea7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fea7-136">RELATED LINKS</span></span>
