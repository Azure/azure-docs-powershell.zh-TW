---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: b351cfaa5d94c7104972158dc9dee6363a7d466b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909942"
---
# <span data-ttu-id="94d11-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="94d11-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="94d11-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94d11-102">SYNOPSIS</span></span>
<span data-ttu-id="94d11-103">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="94d11-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="94d11-104">語法</span><span class="sxs-lookup"><span data-stu-id="94d11-104">SYNTAX</span></span>

### <span data-ttu-id="94d11-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="94d11-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d11-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="94d11-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d11-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="94d11-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d11-108">描述</span><span class="sxs-lookup"><span data-stu-id="94d11-108">DESCRIPTION</span></span>
<span data-ttu-id="94d11-109">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="94d11-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="94d11-110">此動作會使新安裝的安全性代理程式報告至此訂閱的預設工作區。</span><span class="sxs-lookup"><span data-stu-id="94d11-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="94d11-111">例子</span><span class="sxs-lookup"><span data-stu-id="94d11-111">EXAMPLES</span></span>

### <span data-ttu-id="94d11-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="94d11-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="94d11-113">刪除此訂閱的安全性工作區設定。</span><span class="sxs-lookup"><span data-stu-id="94d11-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="94d11-114">參數</span><span class="sxs-lookup"><span data-stu-id="94d11-114">PARAMETERS</span></span>

### <span data-ttu-id="94d11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d11-115">-DefaultProfile</span></span>
<span data-ttu-id="94d11-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94d11-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d11-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94d11-117">-InputObject</span></span>
<span data-ttu-id="94d11-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="94d11-118">Input Object.</span></span>

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

### <span data-ttu-id="94d11-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="94d11-119">-Name</span></span>
<span data-ttu-id="94d11-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="94d11-120">Resource name.</span></span>

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

### <span data-ttu-id="94d11-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94d11-121">-PassThru</span></span>
<span data-ttu-id="94d11-122">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="94d11-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="94d11-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94d11-123">-ResourceId</span></span>
<span data-ttu-id="94d11-124">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="94d11-124">Resource ID.</span></span>

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

### <span data-ttu-id="94d11-125">-確認</span><span class="sxs-lookup"><span data-stu-id="94d11-125">-Confirm</span></span>
<span data-ttu-id="94d11-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94d11-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d11-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d11-127">-WhatIf</span></span>
<span data-ttu-id="94d11-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94d11-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94d11-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94d11-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d11-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d11-130">CommonParameters</span></span>
<span data-ttu-id="94d11-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94d11-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d11-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94d11-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d11-133">輸入</span><span class="sxs-lookup"><span data-stu-id="94d11-133">INPUTS</span></span>

### <span data-ttu-id="94d11-134">System.String</span><span class="sxs-lookup"><span data-stu-id="94d11-134">System.String</span></span>

### <span data-ttu-id="94d11-135">Microsoft.Azure.Commands.security.models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="94d11-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="94d11-136">輸出</span><span class="sxs-lookup"><span data-stu-id="94d11-136">OUTPUTS</span></span>

### <span data-ttu-id="94d11-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94d11-137">System.Boolean</span></span>

## <span data-ttu-id="94d11-138">筆記</span><span class="sxs-lookup"><span data-stu-id="94d11-138">NOTES</span></span>

## <span data-ttu-id="94d11-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="94d11-139">RELATED LINKS</span></span>
