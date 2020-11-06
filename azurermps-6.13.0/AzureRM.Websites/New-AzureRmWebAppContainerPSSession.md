---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445307"
---
# <span data-ttu-id="4ae4e-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="4ae4e-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="4ae4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ae4e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae4e-103">New-AzureRmWebAppContainerPSSession 會在指定的網站或槽和指定的資源群組中，建立新的遠端 PowerShell 會話至指定的 windows 容器中。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ae4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ae4e-104">SYNTAX</span></span>

### <span data-ttu-id="4ae4e-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="4ae4e-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae4e-106">S2</span><span class="sxs-lookup"><span data-stu-id="4ae4e-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae4e-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ae4e-107">DESCRIPTION</span></span>
<span data-ttu-id="4ae4e-108">New-AzureRmWebAppContainerPSSession 會在指定的網站或槽和指定的資源群組中，建立新的遠端 PowerShell 會話至指定的 windows 容器中。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="4ae4e-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ae4e-109">EXAMPLES</span></span>

### <span data-ttu-id="4ae4e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4ae4e-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="4ae4e-111">這會在 windows 容器 app ContosoASP 中建立新的遠端 PowerShell 會話，並顯示在容器上執行的進程 ContosoASP</span><span class="sxs-lookup"><span data-stu-id="4ae4e-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="4ae4e-112">參數</span><span class="sxs-lookup"><span data-stu-id="4ae4e-112">PARAMETERS</span></span>

### <span data-ttu-id="4ae4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae4e-113">-DefaultProfile</span></span>
<span data-ttu-id="4ae4e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae4e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ae4e-115">-Force</span></span>
<span data-ttu-id="4ae4e-116">建立 PowerShell 會話，但不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4ae4e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ae4e-117">-Name</span></span>
<span data-ttu-id="4ae4e-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-118">The name of the web app.</span></span>

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

### <span data-ttu-id="4ae4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ae4e-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ae4e-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="4ae4e-121">-SlotName</span></span>
<span data-ttu-id="4ae4e-122">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="4ae4e-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4ae4e-123">-WebApp</span></span>
<span data-ttu-id="4ae4e-124">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="4ae4e-124">The web app object</span></span>

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

### <span data-ttu-id="4ae4e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4ae4e-125">-Confirm</span></span>
<span data-ttu-id="4ae4e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae4e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae4e-127">-WhatIf</span></span>
<span data-ttu-id="4ae4e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ae4e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae4e-130">CommonParameters</span></span>
<span data-ttu-id="4ae4e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae4e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae4e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4ae4e-133">INPUTS</span></span>

### <span data-ttu-id="4ae4e-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4ae4e-134">System.String</span></span>
### <span data-ttu-id="4ae4e-135">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="4ae4e-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="4ae4e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4ae4e-136">OUTPUTS</span></span>

### <span data-ttu-id="4ae4e-137">System.object</span><span class="sxs-lookup"><span data-stu-id="4ae4e-137">System.String</span></span>
## <span data-ttu-id="4ae4e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4ae4e-138">NOTES</span></span>

## <span data-ttu-id="4ae4e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ae4e-139">RELATED LINKS</span></span>
