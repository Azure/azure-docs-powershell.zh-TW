---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppContainerPSSession.md
ms.openlocfilehash: 2244eb06257d69005d64cc640d0ecd783bd30572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956677"
---
# <span data-ttu-id="4d22a-101">New-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="4d22a-101">New-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="4d22a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d22a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d22a-103">New-AzWebAppContainerPSSession 會在指定的網站或槽和指定的資源群組中，建立新的遠端 PowerShell 會話至指定的 windows 容器中。</span><span class="sxs-lookup"><span data-stu-id="4d22a-103">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="4d22a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d22a-104">SYNTAX</span></span>

### <span data-ttu-id="4d22a-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="4d22a-105">S1 (Default)</span></span>
```
New-AzWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d22a-106">S2</span><span class="sxs-lookup"><span data-stu-id="4d22a-106">S2</span></span>
```
New-AzWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d22a-107">說明</span><span class="sxs-lookup"><span data-stu-id="4d22a-107">DESCRIPTION</span></span>
<span data-ttu-id="4d22a-108">New-AzWebAppContainerPSSession 會在指定的網站或槽和指定的資源群組中，建立新的遠端 PowerShell 會話至指定的 windows 容器中。</span><span class="sxs-lookup"><span data-stu-id="4d22a-108">New-AzWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="4d22a-109">示例</span><span class="sxs-lookup"><span data-stu-id="4d22a-109">EXAMPLES</span></span>

### <span data-ttu-id="4d22a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4d22a-110">Example 1</span></span>
```
PS C:\> $s = New-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="4d22a-111">這會在 windows 容器 app ContosoASP 中建立新的遠端 PowerShell 會話，並顯示在容器上執行的進程 ContosoASP</span><span class="sxs-lookup"><span data-stu-id="4d22a-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="4d22a-112">參數</span><span class="sxs-lookup"><span data-stu-id="4d22a-112">PARAMETERS</span></span>

### <span data-ttu-id="4d22a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d22a-113">-DefaultProfile</span></span>
<span data-ttu-id="4d22a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d22a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d22a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4d22a-115">-Force</span></span>
<span data-ttu-id="4d22a-116">建立 PowerShell 會話，但不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4d22a-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4d22a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d22a-117">-Name</span></span>
<span data-ttu-id="4d22a-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d22a-118">The name of the web app.</span></span>

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

### <span data-ttu-id="4d22a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d22a-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d22a-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d22a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d22a-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="4d22a-121">-SlotName</span></span>
<span data-ttu-id="4d22a-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d22a-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="4d22a-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4d22a-123">-WebApp</span></span>
<span data-ttu-id="4d22a-124">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="4d22a-124">The web app object</span></span>

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

### <span data-ttu-id="4d22a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4d22a-125">-Confirm</span></span>
<span data-ttu-id="4d22a-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d22a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d22a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d22a-127">-WhatIf</span></span>
<span data-ttu-id="4d22a-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d22a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d22a-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d22a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d22a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d22a-130">CommonParameters</span></span>
<span data-ttu-id="4d22a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d22a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d22a-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d22a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d22a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4d22a-133">INPUTS</span></span>

### <span data-ttu-id="4d22a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4d22a-134">System.String</span></span>

### <span data-ttu-id="4d22a-135">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="4d22a-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d22a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4d22a-136">OUTPUTS</span></span>

### <span data-ttu-id="4d22a-137">系統管理. PSSession</span><span class="sxs-lookup"><span data-stu-id="4d22a-137">System.Management.Automation.Runspaces.PSSession</span></span>

## <span data-ttu-id="4d22a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4d22a-138">NOTES</span></span>

## <span data-ttu-id="4d22a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d22a-139">RELATED LINKS</span></span>
