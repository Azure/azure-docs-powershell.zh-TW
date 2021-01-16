---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435988"
---
# <span data-ttu-id="71883-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71883-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="71883-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71883-102">SYNOPSIS</span></span>
<span data-ttu-id="71883-103">移除 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="71883-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="71883-104">句法</span><span class="sxs-lookup"><span data-stu-id="71883-104">SYNTAX</span></span>

### <span data-ttu-id="71883-105">S1</span><span class="sxs-lookup"><span data-stu-id="71883-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71883-106">S2</span><span class="sxs-lookup"><span data-stu-id="71883-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71883-107">說明</span><span class="sxs-lookup"><span data-stu-id="71883-107">DESCRIPTION</span></span>
<span data-ttu-id="71883-108">**AzWebApp** Cmdlet 會移除 Azure Web App 提供的資源群組和 Web app 名稱。</span><span class="sxs-lookup"><span data-stu-id="71883-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="71883-109">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="71883-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="71883-110">示例</span><span class="sxs-lookup"><span data-stu-id="71883-110">EXAMPLES</span></span>

### <span data-ttu-id="71883-111">範例1：移除 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="71883-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="71883-112">這個命令會移除名為 ContosoSite 的 Azure Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="71883-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="71883-113">參數</span><span class="sxs-lookup"><span data-stu-id="71883-113">PARAMETERS</span></span>

### <span data-ttu-id="71883-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71883-114">-AsJob</span></span>
<span data-ttu-id="71883-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71883-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71883-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71883-116">-DefaultProfile</span></span>
<span data-ttu-id="71883-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71883-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71883-118">-Force</span><span class="sxs-lookup"><span data-stu-id="71883-118">-Force</span></span>
<span data-ttu-id="71883-119">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="71883-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="71883-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="71883-120">-Name</span></span>
<span data-ttu-id="71883-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="71883-121">WebApp Name</span></span>

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

### <span data-ttu-id="71883-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71883-122">-ResourceGroupName</span></span>
<span data-ttu-id="71883-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="71883-123">Resource Group Name</span></span>

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

### <span data-ttu-id="71883-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71883-124">-WebApp</span></span>
<span data-ttu-id="71883-125">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="71883-125">WebApp Object</span></span>

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

### <span data-ttu-id="71883-126">-確認</span><span class="sxs-lookup"><span data-stu-id="71883-126">-Confirm</span></span>
<span data-ttu-id="71883-127">在執行 Cmdlet 之前提示您進行確認。在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71883-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71883-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71883-128">-WhatIf</span></span>
<span data-ttu-id="71883-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71883-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71883-130">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71883-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71883-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71883-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71883-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71883-132">CommonParameters</span></span>
<span data-ttu-id="71883-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71883-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71883-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71883-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71883-135">輸入</span><span class="sxs-lookup"><span data-stu-id="71883-135">INPUTS</span></span>

### <span data-ttu-id="71883-136">System.object</span><span class="sxs-lookup"><span data-stu-id="71883-136">System.String</span></span>

### <span data-ttu-id="71883-137">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="71883-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="71883-138">輸出</span><span class="sxs-lookup"><span data-stu-id="71883-138">OUTPUTS</span></span>

### <span data-ttu-id="71883-139">System.void</span><span class="sxs-lookup"><span data-stu-id="71883-139">System.Void</span></span>

## <span data-ttu-id="71883-140">筆記</span><span class="sxs-lookup"><span data-stu-id="71883-140">NOTES</span></span>

## <span data-ttu-id="71883-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="71883-141">RELATED LINKS</span></span>

[<span data-ttu-id="71883-142">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71883-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="71883-143">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71883-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="71883-144">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71883-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="71883-145">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71883-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="71883-146">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="71883-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


