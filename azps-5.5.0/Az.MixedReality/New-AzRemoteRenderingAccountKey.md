---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129118"
---
# <span data-ttu-id="b422a-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="b422a-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="b422a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b422a-102">SYNOPSIS</span></span>
<span data-ttu-id="b422a-103">遠端轉譯帳戶的重新產生鍵</span><span class="sxs-lookup"><span data-stu-id="b422a-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="b422a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b422a-104">SYNTAX</span></span>

### <span data-ttu-id="b422a-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="b422a-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b422a-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="b422a-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b422a-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="b422a-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b422a-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="b422a-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b422a-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="b422a-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b422a-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="b422a-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b422a-111">說明</span><span class="sxs-lookup"><span data-stu-id="b422a-111">DESCRIPTION</span></span>
<span data-ttu-id="b422a-112">重新產生遠端轉譯帳戶的主鍵或輔助鍵。</span><span class="sxs-lookup"><span data-stu-id="b422a-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="b422a-113">示例</span><span class="sxs-lookup"><span data-stu-id="b422a-113">EXAMPLES</span></span>

### <span data-ttu-id="b422a-114">範例1</span><span class="sxs-lookup"><span data-stu-id="b422a-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="b422a-115">在資源群組 "rg1" 中，重新產生遠端轉譯帳戶 "範例" 的輔助金鑰。</span><span class="sxs-lookup"><span data-stu-id="b422a-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="b422a-116">範例2</span><span class="sxs-lookup"><span data-stu-id="b422a-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="b422a-117">從目前的訂閱和含有管道的資源群組 "rg1" 重新產生遠端轉譯帳戶 "範例" 的輔助金鑰。</span><span class="sxs-lookup"><span data-stu-id="b422a-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="b422a-118">參數</span><span class="sxs-lookup"><span data-stu-id="b422a-118">PARAMETERS</span></span>

### <span data-ttu-id="b422a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b422a-119">-DefaultProfile</span></span>
<span data-ttu-id="b422a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b422a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b422a-121">-Force</span></span>
<span data-ttu-id="b422a-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b422a-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b422a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b422a-123">-InputObject</span></span>
<span data-ttu-id="b422a-124">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="b422a-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b422a-125">-Name</span></span>
<span data-ttu-id="b422a-126">遠端轉譯帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b422a-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-127">-主要</span><span class="sxs-lookup"><span data-stu-id="b422a-127">-Primary</span></span>
<span data-ttu-id="b422a-128">重新產生遠端轉譯帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="b422a-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b422a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b422a-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b422a-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b422a-131">-ResourceId</span></span>
<span data-ttu-id="b422a-132">遠端轉譯帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b422a-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-133">-副</span><span class="sxs-lookup"><span data-stu-id="b422a-133">-Secondary</span></span>
<span data-ttu-id="b422a-134">重新產生遠端轉譯帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="b422a-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b422a-135">-確認</span><span class="sxs-lookup"><span data-stu-id="b422a-135">-Confirm</span></span>
<span data-ttu-id="b422a-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b422a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b422a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b422a-137">-WhatIf</span></span>
<span data-ttu-id="b422a-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b422a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b422a-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b422a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b422a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b422a-140">CommonParameters</span></span>
<span data-ttu-id="b422a-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b422a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b422a-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b422a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b422a-143">輸入</span><span class="sxs-lookup"><span data-stu-id="b422a-143">INPUTS</span></span>

### <span data-ttu-id="b422a-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b422a-144">System.String</span></span>

### <span data-ttu-id="b422a-145">MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="b422a-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="b422a-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b422a-146">OUTPUTS</span></span>

### <span data-ttu-id="b422a-147">MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b422a-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="b422a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b422a-148">NOTES</span></span>

## <span data-ttu-id="b422a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b422a-149">RELATED LINKS</span></span>
