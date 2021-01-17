---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286395"
---
# <span data-ttu-id="043c2-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="043c2-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="043c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="043c2-102">SYNOPSIS</span></span>
<span data-ttu-id="043c2-103">授與來源共用的已撤銷共用訂閱存取權</span><span class="sxs-lookup"><span data-stu-id="043c2-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="043c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="043c2-104">SYNTAX</span></span>

### <span data-ttu-id="043c2-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="043c2-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="043c2-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="043c2-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="043c2-107">DESCRIPTION</span></span>
<span data-ttu-id="043c2-108">**Grant AzDataShareSubscriptionAccess** Cmdlet 會授權共用訂閱存取來源共用</span><span class="sxs-lookup"><span data-stu-id="043c2-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="043c2-109">示例</span><span class="sxs-lookup"><span data-stu-id="043c2-109">EXAMPLES</span></span>

### <span data-ttu-id="043c2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="043c2-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="043c2-111">授與識別碼所識別之共用訂閱的存取權8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="043c2-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="043c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="043c2-112">PARAMETERS</span></span>

### <span data-ttu-id="043c2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="043c2-113">-AccountName</span></span>
<span data-ttu-id="043c2-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="043c2-114">Azure data share account name</span></span>

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

### <span data-ttu-id="043c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043c2-115">-DefaultProfile</span></span>
<span data-ttu-id="043c2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="043c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="043c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="043c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="043c2-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="043c2-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="043c2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="043c2-119">-ResourceId</span></span>
<span data-ttu-id="043c2-120">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="043c2-120">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="043c2-121">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="043c2-121">-ShareName</span></span>
<span data-ttu-id="043c2-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="043c2-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043c2-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="043c2-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="043c2-124">提供者共用訂閱的共用訂閱 id</span><span class="sxs-lookup"><span data-stu-id="043c2-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="043c2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="043c2-125">-Confirm</span></span>
<span data-ttu-id="043c2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="043c2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043c2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043c2-127">-WhatIf</span></span>
<span data-ttu-id="043c2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="043c2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="043c2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="043c2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043c2-130">CommonParameters</span></span>
<span data-ttu-id="043c2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="043c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043c2-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="043c2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043c2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="043c2-133">INPUTS</span></span>

### <span data-ttu-id="043c2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="043c2-134">System.String</span></span>

## <span data-ttu-id="043c2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="043c2-135">OUTPUTS</span></span>

### <span data-ttu-id="043c2-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="043c2-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="043c2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="043c2-137">NOTES</span></span>

## <span data-ttu-id="043c2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="043c2-138">RELATED LINKS</span></span>
