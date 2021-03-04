---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 213fbd5e035c48892db1c44fb4ac8de8fbf8bba9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905702"
---
# <span data-ttu-id="ba92f-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="ba92f-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="ba92f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba92f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba92f-103">New-AzWebAppContainerPSSession會建立新的遠端 PowerShell 會話至指定網站或插槽中指定的視窗容器，以及指定資源群組</span><span class="sxs-lookup"><span data-stu-id="ba92f-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ba92f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba92f-104">SYNTAX</span></span>

### <span data-ttu-id="ba92f-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="ba92f-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba92f-106">S2</span><span class="sxs-lookup"><span data-stu-id="ba92f-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba92f-107">描述</span><span class="sxs-lookup"><span data-stu-id="ba92f-107">DESCRIPTION</span></span>
<span data-ttu-id="ba92f-108">New-AzWebAppContainerPSSession會建立新的遠端 PowerShell 會話至指定網站或插槽中指定的視窗容器，以及指定資源群組</span><span class="sxs-lookup"><span data-stu-id="ba92f-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="ba92f-109">例子</span><span class="sxs-lookup"><span data-stu-id="ba92f-109">EXAMPLES</span></span>

### <span data-ttu-id="ba92f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ba92f-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="ba92f-111">這會在 Windows 容器應用程式 ContosoASP 中建立新的遠端 PowerShell 會話，並顯示容器 ContosoASP 上執行的流程</span><span class="sxs-lookup"><span data-stu-id="ba92f-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="ba92f-112">參數</span><span class="sxs-lookup"><span data-stu-id="ba92f-112">PARAMETERS</span></span>

### <span data-ttu-id="ba92f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba92f-113">-DefaultProfile</span></span>
<span data-ttu-id="ba92f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba92f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba92f-115">-強制</span><span class="sxs-lookup"><span data-stu-id="ba92f-115">-Force</span></span>
<span data-ttu-id="ba92f-116">建立 PowerShell 會話，但不提示確認。</span><span class="sxs-lookup"><span data-stu-id="ba92f-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ba92f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba92f-117">-Name</span></span>
<span data-ttu-id="ba92f-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba92f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="ba92f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba92f-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba92f-120">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba92f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ba92f-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ba92f-121">-SlotName</span></span>
<span data-ttu-id="ba92f-122">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba92f-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ba92f-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ba92f-123">-WebApp</span></span>
<span data-ttu-id="ba92f-124">Web App 物件</span><span class="sxs-lookup"><span data-stu-id="ba92f-124">The web app object</span></span>

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

### <span data-ttu-id="ba92f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ba92f-125">-Confirm</span></span>
<span data-ttu-id="ba92f-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba92f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba92f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba92f-127">-WhatIf</span></span>
<span data-ttu-id="ba92f-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba92f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba92f-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba92f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba92f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba92f-130">CommonParameters</span></span>
<span data-ttu-id="ba92f-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba92f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba92f-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ba92f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba92f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ba92f-133">INPUTS</span></span>

### <span data-ttu-id="ba92f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ba92f-134">System.String</span></span>

### <span data-ttu-id="ba92f-135">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ba92f-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ba92f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ba92f-136">OUTPUTS</span></span>

### <span data-ttu-id="ba92f-137">System.Management.Automation.Runspaces.PSSession</span><span class="sxs-lookup"><span data-stu-id="ba92f-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="ba92f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ba92f-138">NOTES</span></span>

## <span data-ttu-id="ba92f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba92f-139">RELATED LINKS</span></span>
