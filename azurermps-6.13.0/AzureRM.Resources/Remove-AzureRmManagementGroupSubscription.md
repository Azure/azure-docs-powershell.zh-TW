---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: 882583c50db8a4b4473bce829aab120a68478434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445484"
---
# <span data-ttu-id="e5a86-101">Remove-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="e5a86-101">Remove-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="e5a86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5a86-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a86-103">從管理群組中移除訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5a86-103">Removes a Subscription from a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5a86-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5a86-104">SYNTAX</span></span>

```
Remove-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a86-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5a86-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a86-106">**AzureRmManagementGroupSubscription** Cmdlet 會從管理群組中移除訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5a86-106">The **Remove-AzureRmManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="e5a86-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5a86-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a86-108">範例 1-從管理群組中移除訂閱</span><span class="sxs-lookup"><span data-stu-id="e5a86-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="e5a86-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5a86-109">PARAMETERS</span></span>

### <span data-ttu-id="e5a86-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a86-110">-DefaultProfile</span></span>
<span data-ttu-id="e5a86-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5a86-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a86-112">-[名]</span><span class="sxs-lookup"><span data-stu-id="e5a86-112">-GroupName</span></span>
<span data-ttu-id="e5a86-113">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="e5a86-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a86-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5a86-114">-PassThru</span></span>
<span data-ttu-id="e5a86-115">`true`成功執行後返回</span><span class="sxs-lookup"><span data-stu-id="e5a86-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="e5a86-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5a86-116">-SubscriptionId</span></span>
<span data-ttu-id="e5a86-117">Witht 管理相關聯之訂閱的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="e5a86-117">Subscription Id of the subscription associated witht the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a86-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e5a86-118">-Confirm</span></span>
<span data-ttu-id="e5a86-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5a86-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a86-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a86-120">-WhatIf</span></span>
<span data-ttu-id="e5a86-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5a86-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5a86-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5a86-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5a86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a86-123">CommonParameters</span></span>
<span data-ttu-id="e5a86-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5a86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a86-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5a86-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a86-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e5a86-126">INPUTS</span></span>

### <span data-ttu-id="e5a86-127">所有</span><span class="sxs-lookup"><span data-stu-id="e5a86-127">None</span></span>

## <span data-ttu-id="e5a86-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e5a86-128">OUTPUTS</span></span>

### <span data-ttu-id="e5a86-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e5a86-129">System.Boolean</span></span>

## <span data-ttu-id="e5a86-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e5a86-130">NOTES</span></span>

## <span data-ttu-id="e5a86-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5a86-131">RELATED LINKS</span></span>
