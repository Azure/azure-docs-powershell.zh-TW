---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: f0de174ac85fb4247ac8af55f8a8ab9cb64d6446
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907298"
---
# <span data-ttu-id="c120a-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c120a-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c120a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c120a-102">SYNOPSIS</span></span>
<span data-ttu-id="c120a-103">在訂閱上獲得已設定的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="c120a-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="c120a-104">語法</span><span class="sxs-lookup"><span data-stu-id="c120a-104">SYNTAX</span></span>

### <span data-ttu-id="c120a-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c120a-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c120a-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c120a-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c120a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c120a-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c120a-108">描述</span><span class="sxs-lookup"><span data-stu-id="c120a-108">DESCRIPTION</span></span>
<span data-ttu-id="c120a-109">此 Cmdlet 可讓您探索已配置的工作區，該工作區會保存此訂閱內安裝于 VMs 中的安全性代理程式所收集的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="c120a-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="c120a-110">例子</span><span class="sxs-lookup"><span data-stu-id="c120a-110">EXAMPLES</span></span>

### <span data-ttu-id="c120a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c120a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="c120a-112">獲得訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="c120a-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="c120a-113">參數</span><span class="sxs-lookup"><span data-stu-id="c120a-113">PARAMETERS</span></span>

### <span data-ttu-id="c120a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c120a-114">-DefaultProfile</span></span>
<span data-ttu-id="c120a-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c120a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c120a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c120a-116">-Name</span></span>
<span data-ttu-id="c120a-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c120a-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c120a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c120a-118">-ResourceId</span></span>
<span data-ttu-id="c120a-119">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c120a-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c120a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c120a-120">CommonParameters</span></span>
<span data-ttu-id="c120a-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c120a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c120a-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c120a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c120a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c120a-123">INPUTS</span></span>

### <span data-ttu-id="c120a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c120a-124">System.String</span></span>

## <span data-ttu-id="c120a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c120a-125">OUTPUTS</span></span>

### <span data-ttu-id="c120a-126">Microsoft.Azure.Commands.security.models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="c120a-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="c120a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c120a-127">NOTES</span></span>

## <span data-ttu-id="c120a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c120a-128">RELATED LINKS</span></span>
