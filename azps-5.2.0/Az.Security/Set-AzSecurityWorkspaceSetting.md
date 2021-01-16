---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 23d35a0bce62aa2a3a5c922ea0e25e35cb619b09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279544"
---
# <span data-ttu-id="b1afc-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b1afc-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b1afc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1afc-102">SYNOPSIS</span></span>
<span data-ttu-id="b1afc-103">更新訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="b1afc-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="b1afc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1afc-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1afc-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1afc-105">DESCRIPTION</span></span>
<span data-ttu-id="b1afc-106">更新訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="b1afc-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="b1afc-107">已設定的工作區會保留由在此訂閱內的 Vm 中安裝的 Azure Log Analytics agent 代理程式所收集的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="b1afc-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="b1afc-108">示例</span><span class="sxs-lookup"><span data-stu-id="b1afc-108">EXAMPLES</span></span>

### <span data-ttu-id="b1afc-109">範例1</span><span class="sxs-lookup"><span data-stu-id="b1afc-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="b1afc-110">設定 "myWorkspace" 工作區，以保留由 Azure Log Analytics 代理程式收集的所有安全性資料。</span><span class="sxs-lookup"><span data-stu-id="b1afc-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="b1afc-111">參數</span><span class="sxs-lookup"><span data-stu-id="b1afc-111">PARAMETERS</span></span>

### <span data-ttu-id="b1afc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1afc-112">-DefaultProfile</span></span>
<span data-ttu-id="b1afc-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1afc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1afc-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1afc-114">-Name</span></span>
<span data-ttu-id="b1afc-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b1afc-115">Resource name.</span></span>

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

### <span data-ttu-id="b1afc-116">-範圍</span><span class="sxs-lookup"><span data-stu-id="b1afc-116">-Scope</span></span>
<span data-ttu-id="b1afc-117">討論.</span><span class="sxs-lookup"><span data-stu-id="b1afc-117">Scope.</span></span>

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

### <span data-ttu-id="b1afc-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b1afc-118">-WorkspaceId</span></span>
<span data-ttu-id="b1afc-119">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1afc-119">Workspace ID.</span></span>

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

### <span data-ttu-id="b1afc-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b1afc-120">-Confirm</span></span>
<span data-ttu-id="b1afc-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1afc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1afc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1afc-122">-WhatIf</span></span>
<span data-ttu-id="b1afc-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1afc-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1afc-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1afc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1afc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1afc-125">CommonParameters</span></span>
<span data-ttu-id="b1afc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1afc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1afc-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1afc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1afc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b1afc-128">INPUTS</span></span>

### <span data-ttu-id="b1afc-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b1afc-129">System.String</span></span>

## <span data-ttu-id="b1afc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b1afc-130">OUTPUTS</span></span>

### <span data-ttu-id="b1afc-131">PSSecurityWorkspaceSetting 中的 WorkspaceSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="b1afc-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b1afc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b1afc-132">NOTES</span></span>

## <span data-ttu-id="b1afc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1afc-133">RELATED LINKS</span></span>
