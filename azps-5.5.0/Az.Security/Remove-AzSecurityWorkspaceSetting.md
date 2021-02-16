---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130807"
---
# <span data-ttu-id="de517-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="de517-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="de517-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de517-102">SYNOPSIS</span></span>
<span data-ttu-id="de517-103">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="de517-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="de517-104">句法</span><span class="sxs-lookup"><span data-stu-id="de517-104">SYNTAX</span></span>

### <span data-ttu-id="de517-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="de517-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de517-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="de517-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de517-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="de517-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de517-108">說明</span><span class="sxs-lookup"><span data-stu-id="de517-108">DESCRIPTION</span></span>
<span data-ttu-id="de517-109">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="de517-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="de517-110">這個動作會讓新安裝的安全代理程式報告到此訂閱的預設工作區。</span><span class="sxs-lookup"><span data-stu-id="de517-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="de517-111">示例</span><span class="sxs-lookup"><span data-stu-id="de517-111">EXAMPLES</span></span>

### <span data-ttu-id="de517-112">範例1</span><span class="sxs-lookup"><span data-stu-id="de517-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="de517-113">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="de517-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="de517-114">參數</span><span class="sxs-lookup"><span data-stu-id="de517-114">PARAMETERS</span></span>

### <span data-ttu-id="de517-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de517-115">-DefaultProfile</span></span>
<span data-ttu-id="de517-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de517-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de517-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de517-117">-InputObject</span></span>
<span data-ttu-id="de517-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="de517-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de517-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="de517-119">-Name</span></span>
<span data-ttu-id="de517-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="de517-120">Resource name.</span></span>

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

### <span data-ttu-id="de517-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de517-121">-PassThru</span></span>
<span data-ttu-id="de517-122">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="de517-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="de517-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de517-123">-ResourceId</span></span>
<span data-ttu-id="de517-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="de517-124">Resource ID.</span></span>

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

### <span data-ttu-id="de517-125">-確認</span><span class="sxs-lookup"><span data-stu-id="de517-125">-Confirm</span></span>
<span data-ttu-id="de517-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de517-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de517-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de517-127">-WhatIf</span></span>
<span data-ttu-id="de517-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de517-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de517-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de517-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de517-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de517-130">CommonParameters</span></span>
<span data-ttu-id="de517-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de517-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de517-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de517-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de517-133">輸入</span><span class="sxs-lookup"><span data-stu-id="de517-133">INPUTS</span></span>

### <span data-ttu-id="de517-134">System.object</span><span class="sxs-lookup"><span data-stu-id="de517-134">System.String</span></span>

### <span data-ttu-id="de517-135">PSSecurityWorkspaceSetting 中的 WorkspaceSettings （Security..。</span><span class="sxs-lookup"><span data-stu-id="de517-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="de517-136">輸出</span><span class="sxs-lookup"><span data-stu-id="de517-136">OUTPUTS</span></span>

### <span data-ttu-id="de517-137">System.object</span><span class="sxs-lookup"><span data-stu-id="de517-137">System.Boolean</span></span>

## <span data-ttu-id="de517-138">筆記</span><span class="sxs-lookup"><span data-stu-id="de517-138">NOTES</span></span>

## <span data-ttu-id="de517-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="de517-139">RELATED LINKS</span></span>
