---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965632"
---
# <span data-ttu-id="171fa-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="171fa-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="171fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="171fa-102">SYNOPSIS</span></span>
<span data-ttu-id="171fa-103">開啟遠端 PowerShell 會話至在指定的網站或槽與指定資源群組中指定的 windows 容器</span><span class="sxs-lookup"><span data-stu-id="171fa-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="171fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="171fa-104">SYNTAX</span></span>

### <span data-ttu-id="171fa-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="171fa-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="171fa-106">S2</span><span class="sxs-lookup"><span data-stu-id="171fa-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="171fa-107">說明</span><span class="sxs-lookup"><span data-stu-id="171fa-107">DESCRIPTION</span></span>
<span data-ttu-id="171fa-108">開啟遠端 PowerShell 會話至在指定的網站或槽與指定資源群組中指定的 windows 容器</span><span class="sxs-lookup"><span data-stu-id="171fa-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="171fa-109">示例</span><span class="sxs-lookup"><span data-stu-id="171fa-109">EXAMPLES</span></span>

### <span data-ttu-id="171fa-110">範例1</span><span class="sxs-lookup"><span data-stu-id="171fa-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="171fa-111">這個命令會開啟遠端 PowerShell 會話至 windows 容器 app ContosoASP</span><span class="sxs-lookup"><span data-stu-id="171fa-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="171fa-112">參數</span><span class="sxs-lookup"><span data-stu-id="171fa-112">PARAMETERS</span></span>

### <span data-ttu-id="171fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171fa-113">-DefaultProfile</span></span>
<span data-ttu-id="171fa-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="171fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="171fa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="171fa-115">-Force</span></span>
<span data-ttu-id="171fa-116">建立 PowerShell 會話，但不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="171fa-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="171fa-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="171fa-117">-Name</span></span>
<span data-ttu-id="171fa-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="171fa-118">The name of the web app.</span></span>

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

### <span data-ttu-id="171fa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="171fa-119">-PassThru</span></span>
<span data-ttu-id="171fa-120">傳回表示成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="171fa-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="171fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="171fa-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="171fa-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="171fa-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="171fa-123">-SlotName</span></span>
<span data-ttu-id="171fa-124">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="171fa-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="171fa-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="171fa-125">-WebApp</span></span>
<span data-ttu-id="171fa-126">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="171fa-126">The web app object</span></span>

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

### <span data-ttu-id="171fa-127">-確認</span><span class="sxs-lookup"><span data-stu-id="171fa-127">-Confirm</span></span>
<span data-ttu-id="171fa-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="171fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="171fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="171fa-129">-WhatIf</span></span>
<span data-ttu-id="171fa-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="171fa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="171fa-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="171fa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="171fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171fa-132">CommonParameters</span></span>
<span data-ttu-id="171fa-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="171fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171fa-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="171fa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171fa-135">輸入</span><span class="sxs-lookup"><span data-stu-id="171fa-135">INPUTS</span></span>

### <span data-ttu-id="171fa-136">System.object</span><span class="sxs-lookup"><span data-stu-id="171fa-136">System.String</span></span>

### <span data-ttu-id="171fa-137">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="171fa-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="171fa-138">輸出</span><span class="sxs-lookup"><span data-stu-id="171fa-138">OUTPUTS</span></span>

### <span data-ttu-id="171fa-139">System.void</span><span class="sxs-lookup"><span data-stu-id="171fa-139">System.Void</span></span>

## <span data-ttu-id="171fa-140">筆記</span><span class="sxs-lookup"><span data-stu-id="171fa-140">NOTES</span></span>

## <span data-ttu-id="171fa-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="171fa-141">RELATED LINKS</span></span>