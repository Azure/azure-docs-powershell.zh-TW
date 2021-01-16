---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281892"
---
# <span data-ttu-id="307a1-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="307a1-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="307a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="307a1-102">SYNOPSIS</span></span>
<span data-ttu-id="307a1-103">撤銷共用訂閱對來源共用的存取權</span><span class="sxs-lookup"><span data-stu-id="307a1-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="307a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="307a1-104">SYNTAX</span></span>

### <span data-ttu-id="307a1-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="307a1-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="307a1-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="307a1-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="307a1-107">說明</span><span class="sxs-lookup"><span data-stu-id="307a1-107">DESCRIPTION</span></span>
<span data-ttu-id="307a1-108">**AzDataShareSubscriptionAccess** Cmdlet 會授權共用訂閱存取來源共用</span><span class="sxs-lookup"><span data-stu-id="307a1-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="307a1-109">示例</span><span class="sxs-lookup"><span data-stu-id="307a1-109">EXAMPLES</span></span>

### <span data-ttu-id="307a1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="307a1-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="307a1-111">撤銷由識別碼8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 識別的共用訂閱的存取權</span><span class="sxs-lookup"><span data-stu-id="307a1-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="307a1-112">參數</span><span class="sxs-lookup"><span data-stu-id="307a1-112">PARAMETERS</span></span>

### <span data-ttu-id="307a1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="307a1-113">-AccountName</span></span>
<span data-ttu-id="307a1-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="307a1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="307a1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="307a1-115">-AsJob</span></span>
<span data-ttu-id="307a1-116">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="307a1-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="307a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307a1-117">-DefaultProfile</span></span>
<span data-ttu-id="307a1-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="307a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="307a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="307a1-120">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="307a1-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="307a1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="307a1-121">-ResourceId</span></span>
<span data-ttu-id="307a1-122">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="307a1-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="307a1-123">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="307a1-123">-ShareName</span></span>
<span data-ttu-id="307a1-124">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="307a1-124">Azure data share name</span></span>

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

### <span data-ttu-id="307a1-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="307a1-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="307a1-126">提供者共用訂閱的共用訂閱 id</span><span class="sxs-lookup"><span data-stu-id="307a1-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="307a1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="307a1-127">-Confirm</span></span>
<span data-ttu-id="307a1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="307a1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="307a1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="307a1-129">-WhatIf</span></span>
<span data-ttu-id="307a1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="307a1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="307a1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="307a1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="307a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307a1-132">CommonParameters</span></span>
<span data-ttu-id="307a1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="307a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307a1-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="307a1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307a1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="307a1-135">INPUTS</span></span>

### <span data-ttu-id="307a1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="307a1-136">System.String</span></span>

## <span data-ttu-id="307a1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="307a1-137">OUTPUTS</span></span>

### <span data-ttu-id="307a1-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="307a1-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="307a1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="307a1-139">NOTES</span></span>

## <span data-ttu-id="307a1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="307a1-140">RELATED LINKS</span></span>
