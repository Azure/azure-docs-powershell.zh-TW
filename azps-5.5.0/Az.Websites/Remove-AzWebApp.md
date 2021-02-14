---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130238"
---
# <span data-ttu-id="c4004-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="c4004-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4004-102">SYNOPSIS</span></span>
<span data-ttu-id="c4004-103">移除 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c4004-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="c4004-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4004-104">SYNTAX</span></span>

### <span data-ttu-id="c4004-105">S1</span><span class="sxs-lookup"><span data-stu-id="c4004-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4004-106">S2</span><span class="sxs-lookup"><span data-stu-id="c4004-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4004-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4004-107">DESCRIPTION</span></span>
<span data-ttu-id="c4004-108">**AzWebApp** Cmdlet 會移除 Azure Web App 提供的資源群組和 Web app 名稱。</span><span class="sxs-lookup"><span data-stu-id="c4004-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="c4004-109">這個 Cmdlet 預設會同時移除所有的槽與躍點數。</span><span class="sxs-lookup"><span data-stu-id="c4004-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="c4004-110">示例</span><span class="sxs-lookup"><span data-stu-id="c4004-110">EXAMPLES</span></span>

### <span data-ttu-id="c4004-111">範例1：移除 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="c4004-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c4004-112">這個命令會移除名為 ContosoSite 的 Azure Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c4004-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c4004-113">參數</span><span class="sxs-lookup"><span data-stu-id="c4004-113">PARAMETERS</span></span>

### <span data-ttu-id="c4004-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4004-114">-AsJob</span></span>
<span data-ttu-id="c4004-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4004-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4004-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4004-116">-DefaultProfile</span></span>
<span data-ttu-id="c4004-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4004-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4004-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c4004-118">-Force</span></span>
<span data-ttu-id="c4004-119">[強制移除] 選項</span><span class="sxs-lookup"><span data-stu-id="c4004-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="c4004-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4004-120">-Name</span></span>
<span data-ttu-id="c4004-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c4004-121">WebApp Name</span></span>

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

### <span data-ttu-id="c4004-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4004-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4004-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c4004-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c4004-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-124">-WebApp</span></span>
<span data-ttu-id="c4004-125">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c4004-125">WebApp Object</span></span>

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

### <span data-ttu-id="c4004-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c4004-126">-Confirm</span></span>
<span data-ttu-id="c4004-127">在執行 Cmdlet 之前提示您進行確認。在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4004-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4004-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4004-128">-WhatIf</span></span>
<span data-ttu-id="c4004-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4004-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4004-130">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4004-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4004-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4004-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4004-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4004-132">CommonParameters</span></span>
<span data-ttu-id="c4004-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4004-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4004-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4004-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4004-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c4004-135">INPUTS</span></span>

### <span data-ttu-id="c4004-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c4004-136">System.String</span></span>

### <span data-ttu-id="c4004-137">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="c4004-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c4004-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c4004-138">OUTPUTS</span></span>

### <span data-ttu-id="c4004-139">System.void</span><span class="sxs-lookup"><span data-stu-id="c4004-139">System.Void</span></span>

## <span data-ttu-id="c4004-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c4004-140">NOTES</span></span>

## <span data-ttu-id="c4004-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4004-141">RELATED LINKS</span></span>

[<span data-ttu-id="c4004-142">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c4004-143">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c4004-144">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c4004-145">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c4004-146">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c4004-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


