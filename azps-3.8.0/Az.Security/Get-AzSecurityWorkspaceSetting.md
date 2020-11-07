---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 5b905083668392ce026bfa416252eb1371ebb640
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957531"
---
# <span data-ttu-id="af8b9-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="af8b9-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="af8b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="af8b9-103">取得訂閱上已設定的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="af8b9-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="af8b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="af8b9-104">SYNTAX</span></span>

### <span data-ttu-id="af8b9-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="af8b9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af8b9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="af8b9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af8b9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="af8b9-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af8b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="af8b9-108">DESCRIPTION</span></span>
<span data-ttu-id="af8b9-109">這個 Cmdlet 可讓您探索已設定的工作區，以保留此訂閱內 Vm 中安裝的安全代理程式所收集的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="af8b9-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="af8b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="af8b9-110">EXAMPLES</span></span>

### <span data-ttu-id="af8b9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="af8b9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="af8b9-112">取得訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="af8b9-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="af8b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="af8b9-113">PARAMETERS</span></span>

### <span data-ttu-id="af8b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8b9-114">-DefaultProfile</span></span>
<span data-ttu-id="af8b9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af8b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af8b9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="af8b9-116">-Name</span></span>
<span data-ttu-id="af8b9-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="af8b9-117">Resource name.</span></span>

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

### <span data-ttu-id="af8b9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af8b9-118">-ResourceId</span></span>
<span data-ttu-id="af8b9-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="af8b9-119">Resource ID.</span></span>

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

### <span data-ttu-id="af8b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8b9-120">CommonParameters</span></span>
<span data-ttu-id="af8b9-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af8b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8b9-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af8b9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8b9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="af8b9-123">INPUTS</span></span>

### <span data-ttu-id="af8b9-124">System.object</span><span class="sxs-lookup"><span data-stu-id="af8b9-124">System.String</span></span>

## <span data-ttu-id="af8b9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="af8b9-125">OUTPUTS</span></span>

### <span data-ttu-id="af8b9-126">PSSecurityWorkspaceSetting 中的 WorkspaceSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="af8b9-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="af8b9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="af8b9-127">NOTES</span></span>

## <span data-ttu-id="af8b9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="af8b9-128">RELATED LINKS</span></span>
