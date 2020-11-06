---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451067"
---
# <span data-ttu-id="a3b3d-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="a3b3d-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="a3b3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b3d-103">更新訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3b3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3b3d-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b3d-106">更新訂閱的工作區設定。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="a3b3d-107">已設定的工作區會保留此訂閱中安裝在 Vm 中的安全代理程式所收集的安全性資料。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="a3b3d-108">示例</span><span class="sxs-lookup"><span data-stu-id="a3b3d-108">EXAMPLES</span></span>

### <span data-ttu-id="a3b3d-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a3b3d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="a3b3d-110">設定 "myWorkspace" 工作區，以保留安全代理程式收集的所有安全性資料。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="a3b3d-111">參數</span><span class="sxs-lookup"><span data-stu-id="a3b3d-111">PARAMETERS</span></span>

### <span data-ttu-id="a3b3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b3d-112">-DefaultProfile</span></span>
<span data-ttu-id="a3b3d-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3b3d-114">-Name</span></span>
<span data-ttu-id="a3b3d-115">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-116">-範圍</span><span class="sxs-lookup"><span data-stu-id="a3b3d-116">-Scope</span></span>
<span data-ttu-id="a3b3d-117">討論.</span><span class="sxs-lookup"><span data-stu-id="a3b3d-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a3b3d-118">-WorkspaceId</span></span>
<span data-ttu-id="a3b3d-119">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-120">-確認</span><span class="sxs-lookup"><span data-stu-id="a3b3d-120">-Confirm</span></span>
<span data-ttu-id="a3b3d-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b3d-122">-WhatIf</span></span>
<span data-ttu-id="a3b3d-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3b3d-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b3d-125">CommonParameters</span></span>
<span data-ttu-id="a3b3d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b3d-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b3d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a3b3d-128">INPUTS</span></span>

### <span data-ttu-id="a3b3d-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a3b3d-129">System.String</span></span>

## <span data-ttu-id="a3b3d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a3b3d-130">OUTPUTS</span></span>

### <span data-ttu-id="a3b3d-131">PSSecurityWorkspaceSetting 中的 WorkspaceSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="a3b3d-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="a3b3d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a3b3d-132">NOTES</span></span>

## <span data-ttu-id="a3b3d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3b3d-133">RELATED LINKS</span></span>
