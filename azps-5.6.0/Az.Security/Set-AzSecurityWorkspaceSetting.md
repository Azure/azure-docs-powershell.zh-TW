---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 6bcee25399004d5fb8f485e9c58446713bedc5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915886"
---
# <span data-ttu-id="04b94-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="04b94-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="04b94-102">簡介</span><span class="sxs-lookup"><span data-stu-id="04b94-102">SYNOPSIS</span></span>
<span data-ttu-id="04b94-103">更新訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="04b94-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="04b94-104">語法</span><span class="sxs-lookup"><span data-stu-id="04b94-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b94-105">描述</span><span class="sxs-lookup"><span data-stu-id="04b94-105">DESCRIPTION</span></span>
<span data-ttu-id="04b94-106">更新訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="04b94-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="04b94-107">已配置的工作區會保留此訂閱內安裝于虛擬機器中的 Azure Log Analytics 代理程式所收集的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="04b94-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="04b94-108">例子</span><span class="sxs-lookup"><span data-stu-id="04b94-108">EXAMPLES</span></span>

### <span data-ttu-id="04b94-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="04b94-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="04b94-110">將 「securityuserws」 工作區設定為保留 Azure 記錄分析代理程式所收集的所有安全性資料。</span><span class="sxs-lookup"><span data-stu-id="04b94-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="04b94-111">參數</span><span class="sxs-lookup"><span data-stu-id="04b94-111">PARAMETERS</span></span>

### <span data-ttu-id="04b94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b94-112">-DefaultProfile</span></span>
<span data-ttu-id="04b94-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="04b94-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b94-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="04b94-114">-Name</span></span>
<span data-ttu-id="04b94-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="04b94-115">Resource name.</span></span>

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

### <span data-ttu-id="04b94-116">-範圍</span><span class="sxs-lookup"><span data-stu-id="04b94-116">-Scope</span></span>
<span data-ttu-id="04b94-117">範圍。</span><span class="sxs-lookup"><span data-stu-id="04b94-117">Scope.</span></span>

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

### <span data-ttu-id="04b94-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="04b94-118">-WorkspaceId</span></span>
<span data-ttu-id="04b94-119">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="04b94-119">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b94-120">-確認</span><span class="sxs-lookup"><span data-stu-id="04b94-120">-Confirm</span></span>
<span data-ttu-id="04b94-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="04b94-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b94-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b94-122">-WhatIf</span></span>
<span data-ttu-id="04b94-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04b94-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04b94-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04b94-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b94-125">CommonParameters</span></span>
<span data-ttu-id="04b94-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="04b94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b94-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b94-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b94-128">輸入</span><span class="sxs-lookup"><span data-stu-id="04b94-128">INPUTS</span></span>

### <span data-ttu-id="04b94-129">System.String</span><span class="sxs-lookup"><span data-stu-id="04b94-129">System.String</span></span>

## <span data-ttu-id="04b94-130">輸出</span><span class="sxs-lookup"><span data-stu-id="04b94-130">OUTPUTS</span></span>

### <span data-ttu-id="04b94-131">Microsoft.Azure.Commands.security.models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="04b94-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="04b94-132">筆記</span><span class="sxs-lookup"><span data-stu-id="04b94-132">NOTES</span></span>

## <span data-ttu-id="04b94-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="04b94-133">RELATED LINKS</span></span>
