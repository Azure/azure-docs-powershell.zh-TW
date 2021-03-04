---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916658"
---
# <span data-ttu-id="a5a28-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="a5a28-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="a5a28-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5a28-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a28-103">移除 Azure 自動化原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5a28-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="a5a28-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5a28-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a28-105">描述</span><span class="sxs-lookup"><span data-stu-id="a5a28-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a28-106">此Remove-AzAutomationSourceControl Cmdlet 會從 Azure Automation 移除原始程式碼管理。</span><span class="sxs-lookup"><span data-stu-id="a5a28-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="a5a28-107">例子</span><span class="sxs-lookup"><span data-stu-id="a5a28-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a28-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5a28-108">Example 1</span></span>
<span data-ttu-id="a5a28-109">此命令會移除名為 devAccount 的帳戶中名為 VSTSNative 的自動化原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5a28-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="a5a28-110">此命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5a28-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="a5a28-111">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5a28-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="a5a28-112">參數</span><span class="sxs-lookup"><span data-stu-id="a5a28-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a28-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5a28-113">-AutomationAccountName</span></span>
<span data-ttu-id="a5a28-114">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a28-114">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a28-115">-DefaultProfile</span></span>
<span data-ttu-id="a5a28-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5a28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a28-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5a28-117">-Name</span></span>
<span data-ttu-id="a5a28-118">原始程式碼管理名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a28-118">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a28-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5a28-119">-PassThru</span></span>
<span data-ttu-id="a5a28-120">PassThru 會傳回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a5a28-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5a28-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a5a28-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a28-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5a28-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a5a28-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a28-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a5a28-124">-Confirm</span></span>
<span data-ttu-id="a5a28-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5a28-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a28-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a28-126">-WhatIf</span></span>
<span data-ttu-id="a5a28-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5a28-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a28-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5a28-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a28-129">CommonParameters</span></span>
<span data-ttu-id="a5a28-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5a28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a28-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a5a28-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a28-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a5a28-132">INPUTS</span></span>

### <span data-ttu-id="a5a28-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a5a28-133">System.String</span></span>

## <span data-ttu-id="a5a28-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a5a28-134">OUTPUTS</span></span>

### <span data-ttu-id="a5a28-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="a5a28-135">System.Void</span></span>

### <span data-ttu-id="a5a28-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5a28-136">System.Boolean</span></span>

## <span data-ttu-id="a5a28-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a5a28-137">NOTES</span></span>

## <span data-ttu-id="a5a28-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5a28-138">RELATED LINKS</span></span>
