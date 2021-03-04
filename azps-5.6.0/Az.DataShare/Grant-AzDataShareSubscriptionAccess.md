---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 00b82731e807aa2351d66744b889f56f440226b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916146"
---
# <span data-ttu-id="71765-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="71765-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="71765-102">簡介</span><span class="sxs-lookup"><span data-stu-id="71765-102">SYNOPSIS</span></span>
<span data-ttu-id="71765-103">授予已撤銷的共用訂閱存取權至來源共用</span><span class="sxs-lookup"><span data-stu-id="71765-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="71765-104">語法</span><span class="sxs-lookup"><span data-stu-id="71765-104">SYNTAX</span></span>

### <span data-ttu-id="71765-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71765-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71765-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71765-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71765-107">描述</span><span class="sxs-lookup"><span data-stu-id="71765-107">DESCRIPTION</span></span>
<span data-ttu-id="71765-108">**Grant-AzDataShareSubscriptionAccess** Cmdlet 會授予來源共用的共用訂閱存取權</span><span class="sxs-lookup"><span data-stu-id="71765-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="71765-109">例子</span><span class="sxs-lookup"><span data-stu-id="71765-109">EXAMPLES</span></span>

### <span data-ttu-id="71765-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="71765-110">Example 1</span></span>
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

<span data-ttu-id="71765-111">授予以 id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 識別的共用訂閱存取權</span><span class="sxs-lookup"><span data-stu-id="71765-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="71765-112">參數</span><span class="sxs-lookup"><span data-stu-id="71765-112">PARAMETERS</span></span>

### <span data-ttu-id="71765-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71765-113">-AccountName</span></span>
<span data-ttu-id="71765-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="71765-114">Azure data share account name</span></span>

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

### <span data-ttu-id="71765-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71765-115">-DefaultProfile</span></span>
<span data-ttu-id="71765-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="71765-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71765-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71765-117">-ResourceGroupName</span></span>
<span data-ttu-id="71765-118">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="71765-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="71765-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71765-119">-ResourceId</span></span>
<span data-ttu-id="71765-120">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="71765-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="71765-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="71765-121">-ShareName</span></span>
<span data-ttu-id="71765-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="71765-122">Azure data share name</span></span>

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

### <span data-ttu-id="71765-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71765-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="71765-124">提供者共用訂閱的共用訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="71765-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="71765-125">-確認</span><span class="sxs-lookup"><span data-stu-id="71765-125">-Confirm</span></span>
<span data-ttu-id="71765-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="71765-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71765-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71765-127">-WhatIf</span></span>
<span data-ttu-id="71765-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71765-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71765-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71765-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71765-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71765-130">CommonParameters</span></span>
<span data-ttu-id="71765-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="71765-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71765-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71765-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71765-133">輸入</span><span class="sxs-lookup"><span data-stu-id="71765-133">INPUTS</span></span>

### <span data-ttu-id="71765-134">System.String</span><span class="sxs-lookup"><span data-stu-id="71765-134">System.String</span></span>

## <span data-ttu-id="71765-135">輸出</span><span class="sxs-lookup"><span data-stu-id="71765-135">OUTPUTS</span></span>

### <span data-ttu-id="71765-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="71765-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="71765-137">筆記</span><span class="sxs-lookup"><span data-stu-id="71765-137">NOTES</span></span>

## <span data-ttu-id="71765-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="71765-138">RELATED LINKS</span></span>
