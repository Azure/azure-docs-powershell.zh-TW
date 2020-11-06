---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: a3c75c653d75a4fde969672a245644ee04412731
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443700"
---
# <span data-ttu-id="a3f92-101">New-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="a3f92-101">New-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="a3f92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3f92-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f92-103">新增訂閱給管理群組。</span><span class="sxs-lookup"><span data-stu-id="a3f92-103">Adds a Subscription to a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3f92-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3f92-104">SYNTAX</span></span>

```
New-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f92-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3f92-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f92-106">**AzureRMManagementGroupSubscription** Cmdlet 會新增訂閱給管理群組。</span><span class="sxs-lookup"><span data-stu-id="a3f92-106">The **New-AzureRMManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="a3f92-107">示例</span><span class="sxs-lookup"><span data-stu-id="a3f92-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f92-108">範例1：新增訂閱至管理群組</span><span class="sxs-lookup"><span data-stu-id="a3f92-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzureRMManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="a3f92-109">參數</span><span class="sxs-lookup"><span data-stu-id="a3f92-109">PARAMETERS</span></span>

### <span data-ttu-id="a3f92-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f92-110">-DefaultProfile</span></span>
<span data-ttu-id="a3f92-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3f92-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3f92-112">-[名]</span><span class="sxs-lookup"><span data-stu-id="a3f92-112">-GroupName</span></span>
<span data-ttu-id="a3f92-113">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f92-113">Management Group Id</span></span>

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

### <span data-ttu-id="a3f92-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3f92-114">-PassThru</span></span>
<span data-ttu-id="a3f92-115">`true`成功執行後返回</span><span class="sxs-lookup"><span data-stu-id="a3f92-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="a3f92-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3f92-116">-SubscriptionId</span></span>
<span data-ttu-id="a3f92-117">Witht 管理相關聯之訂閱的訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="a3f92-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="a3f92-118">-確認</span><span class="sxs-lookup"><span data-stu-id="a3f92-118">-Confirm</span></span>
<span data-ttu-id="a3f92-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3f92-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3f92-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f92-120">-WhatIf</span></span>
<span data-ttu-id="a3f92-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3f92-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f92-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3f92-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3f92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f92-123">CommonParameters</span></span>
<span data-ttu-id="a3f92-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3f92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f92-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3f92-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f92-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a3f92-126">INPUTS</span></span>

### <span data-ttu-id="a3f92-127">所有</span><span class="sxs-lookup"><span data-stu-id="a3f92-127">None</span></span>

## <span data-ttu-id="a3f92-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a3f92-128">OUTPUTS</span></span>

### <span data-ttu-id="a3f92-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a3f92-129">System.Boolean</span></span>

## <span data-ttu-id="a3f92-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a3f92-130">NOTES</span></span>

## <span data-ttu-id="a3f92-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3f92-131">RELATED LINKS</span></span>
