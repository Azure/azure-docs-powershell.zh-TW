---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: ef14039cc1f46c3a891090475814d6e9553da431
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916089"
---
# <span data-ttu-id="c6240-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="c6240-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="c6240-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6240-102">SYNOPSIS</span></span>
<span data-ttu-id="c6240-103">刪除遠端呈現帳戶</span><span class="sxs-lookup"><span data-stu-id="c6240-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="c6240-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6240-104">SYNTAX</span></span>

### <span data-ttu-id="c6240-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c6240-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6240-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6240-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6240-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6240-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6240-108">描述</span><span class="sxs-lookup"><span data-stu-id="c6240-108">DESCRIPTION</span></span>
<span data-ttu-id="c6240-109">刪除特定訂閱和資源群組中指定的遠端呈現帳戶。</span><span class="sxs-lookup"><span data-stu-id="c6240-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="c6240-110">例子</span><span class="sxs-lookup"><span data-stu-id="c6240-110">EXAMPLES</span></span>

### <span data-ttu-id="c6240-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c6240-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="c6240-112">從目前的訂閱和資源群組 "rg1" 刪除遠端呈現帳戶的「範例」。</span><span class="sxs-lookup"><span data-stu-id="c6240-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="c6240-113">參數</span><span class="sxs-lookup"><span data-stu-id="c6240-113">PARAMETERS</span></span>

### <span data-ttu-id="c6240-114">-確認</span><span class="sxs-lookup"><span data-stu-id="c6240-114">-Confirm</span></span>
<span data-ttu-id="c6240-115">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6240-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6240-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6240-116">-DefaultProfile</span></span>
<span data-ttu-id="c6240-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6240-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6240-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6240-118">-InputObject</span></span>
<span data-ttu-id="c6240-119">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="c6240-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6240-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6240-120">-Name</span></span>
<span data-ttu-id="c6240-121">遠端呈現帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c6240-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6240-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6240-122">-PassThru</span></span>
<span data-ttu-id="c6240-123">如果指定，則 Return 物件。</span><span class="sxs-lookup"><span data-stu-id="c6240-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6240-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6240-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6240-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c6240-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6240-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6240-126">-ResourceId</span></span>
<span data-ttu-id="c6240-127">遠端呈現帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6240-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6240-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6240-128">-WhatIf</span></span>
<span data-ttu-id="c6240-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6240-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6240-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6240-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6240-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6240-131">CommonParameters</span></span>
<span data-ttu-id="c6240-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6240-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c6240-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c6240-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6240-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c6240-134">INPUTS</span></span>

### <span data-ttu-id="c6240-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c6240-135">System.String</span></span>

### <span data-ttu-id="c6240-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="c6240-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="c6240-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c6240-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c6240-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c6240-138">OUTPUTS</span></span>

### <span data-ttu-id="c6240-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6240-139">System.Boolean</span></span>

## <span data-ttu-id="c6240-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c6240-140">NOTES</span></span>

## <span data-ttu-id="c6240-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6240-141">RELATED LINKS</span></span>
