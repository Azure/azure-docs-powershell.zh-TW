---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445315"
---
# <span data-ttu-id="a66d5-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="a66d5-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="a66d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a66d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a66d5-103">開啟遠端 PowerShell 會話至在指定的網站或槽與指定資源群組中指定的 windows 容器</span><span class="sxs-lookup"><span data-stu-id="a66d5-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a66d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a66d5-104">SYNTAX</span></span>

### <span data-ttu-id="a66d5-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="a66d5-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a66d5-106">S2</span><span class="sxs-lookup"><span data-stu-id="a66d5-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a66d5-107">說明</span><span class="sxs-lookup"><span data-stu-id="a66d5-107">DESCRIPTION</span></span>
<span data-ttu-id="a66d5-108">開啟遠端 PowerShell 會話至在指定的網站或槽與指定資源群組中指定的 windows 容器</span><span class="sxs-lookup"><span data-stu-id="a66d5-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="a66d5-109">示例</span><span class="sxs-lookup"><span data-stu-id="a66d5-109">EXAMPLES</span></span>

### <span data-ttu-id="a66d5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a66d5-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a66d5-111">這個命令會開啟遠端 PowerShell 會話至 windows 容器 app ContosoASP</span><span class="sxs-lookup"><span data-stu-id="a66d5-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="a66d5-112">參數</span><span class="sxs-lookup"><span data-stu-id="a66d5-112">PARAMETERS</span></span>

### <span data-ttu-id="a66d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66d5-113">-DefaultProfile</span></span>
<span data-ttu-id="a66d5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a66d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a66d5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a66d5-115">-Force</span></span>
<span data-ttu-id="a66d5-116">建立 PowerShell 會話，但不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a66d5-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a66d5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a66d5-117">-Name</span></span>
<span data-ttu-id="a66d5-118">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a66d5-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a66d5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a66d5-119">-PassThru</span></span>
<span data-ttu-id="a66d5-120">傳回表示成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="a66d5-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="a66d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a66d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="a66d5-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a66d5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="a66d5-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a66d5-123">-SlotName</span></span>
<span data-ttu-id="a66d5-124">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="a66d5-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a66d5-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a66d5-125">-WebApp</span></span>
<span data-ttu-id="a66d5-126">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="a66d5-126">The web app object</span></span>

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

### <span data-ttu-id="a66d5-127">-確認</span><span class="sxs-lookup"><span data-stu-id="a66d5-127">-Confirm</span></span>
<span data-ttu-id="a66d5-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a66d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a66d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66d5-129">-WhatIf</span></span>
<span data-ttu-id="a66d5-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a66d5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a66d5-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a66d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a66d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66d5-132">CommonParameters</span></span>
<span data-ttu-id="a66d5-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a66d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66d5-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a66d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66d5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a66d5-135">INPUTS</span></span>

### <span data-ttu-id="a66d5-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a66d5-136">System.String</span></span>
### <span data-ttu-id="a66d5-137">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a66d5-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="a66d5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a66d5-138">OUTPUTS</span></span>

### <span data-ttu-id="a66d5-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a66d5-139">System.String</span></span>
## <span data-ttu-id="a66d5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a66d5-140">NOTES</span></span>

## <span data-ttu-id="a66d5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="a66d5-141">RELATED LINKS</span></span>
