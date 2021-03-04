---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: e889e3f8d3d94993494c10141629eee6dceed01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907018"
---
# <span data-ttu-id="b7cd0-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="b7cd0-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="b7cd0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cd0-103">將遠端 PowerShell 會話開啟到指定網站或插槽及指定資源群組中指定的視窗容器</span><span class="sxs-lookup"><span data-stu-id="b7cd0-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b7cd0-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7cd0-104">SYNTAX</span></span>

### <span data-ttu-id="b7cd0-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="b7cd0-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7cd0-106">S2</span><span class="sxs-lookup"><span data-stu-id="b7cd0-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7cd0-107">描述</span><span class="sxs-lookup"><span data-stu-id="b7cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="b7cd0-108">將遠端 PowerShell 會話開啟到指定網站或插槽及指定資源群組中指定的視窗容器</span><span class="sxs-lookup"><span data-stu-id="b7cd0-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="b7cd0-109">例子</span><span class="sxs-lookup"><span data-stu-id="b7cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="b7cd0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="b7cd0-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="b7cd0-111">此命令會開啟遠端 PowerShell 會話至 Windows 容器應用程式 ContosoASP</span><span class="sxs-lookup"><span data-stu-id="b7cd0-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="b7cd0-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7cd0-112">PARAMETERS</span></span>

### <span data-ttu-id="b7cd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cd0-113">-DefaultProfile</span></span>
<span data-ttu-id="b7cd0-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7cd0-115">-強制</span><span class="sxs-lookup"><span data-stu-id="b7cd0-115">-Force</span></span>
<span data-ttu-id="b7cd0-116">建立 PowerShell 會話，但不提示確認。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b7cd0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7cd0-117">-Name</span></span>
<span data-ttu-id="b7cd0-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7cd0-119">-PassThru</span></span>
<span data-ttu-id="b7cd0-120">返回指出成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="b7cd0-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="b7cd0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cd0-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7cd0-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd0-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="b7cd0-123">-SlotName</span></span>
<span data-ttu-id="b7cd0-124">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd0-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b7cd0-125">-WebApp</span></span>
<span data-ttu-id="b7cd0-126">Web App 物件</span><span class="sxs-lookup"><span data-stu-id="b7cd0-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b7cd0-127">-Confirm</span></span>
<span data-ttu-id="b7cd0-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7cd0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7cd0-129">-WhatIf</span></span>
<span data-ttu-id="b7cd0-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7cd0-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7cd0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cd0-132">CommonParameters</span></span>
<span data-ttu-id="b7cd0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cd0-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b7cd0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cd0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b7cd0-135">INPUTS</span></span>

### <span data-ttu-id="b7cd0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b7cd0-136">System.String</span></span>

### <span data-ttu-id="b7cd0-137">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b7cd0-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b7cd0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b7cd0-138">OUTPUTS</span></span>

### <span data-ttu-id="b7cd0-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="b7cd0-139">System.Void</span></span>

## <span data-ttu-id="b7cd0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b7cd0-140">NOTES</span></span>

## <span data-ttu-id="b7cd0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7cd0-141">RELATED LINKS</span></span>
