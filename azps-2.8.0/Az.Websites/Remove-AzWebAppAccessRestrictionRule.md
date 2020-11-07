---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793320"
---
# <span data-ttu-id="a0535-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a0535-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="a0535-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0535-102">SYNOPSIS</span></span>
<span data-ttu-id="a0535-103">從 Azure Web App 移除訪問限制規則。</span><span class="sxs-lookup"><span data-stu-id="a0535-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="a0535-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0535-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0535-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0535-105">DESCRIPTION</span></span>
<span data-ttu-id="a0535-106">**AzWebAppAccessRestrictionRule** Cmdlet 會從 Azure Web App 中移除訪問限制規則</span><span class="sxs-lookup"><span data-stu-id="a0535-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="a0535-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0535-107">EXAMPLES</span></span>

### <span data-ttu-id="a0535-108">範例1：移除 Web 應用程式存取限制規則</span><span class="sxs-lookup"><span data-stu-id="a0535-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="a0535-109">這個命令會從 Azure Web App 中移除名為「Default-Web-WestUS」的資源群組的 IpRule 存取限制規則。</span><span class="sxs-lookup"><span data-stu-id="a0535-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a0535-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0535-110">PARAMETERS</span></span>

### <span data-ttu-id="a0535-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0535-111">-DefaultProfile</span></span>
<span data-ttu-id="a0535-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0535-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0535-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0535-113">-Name</span></span>
<span data-ttu-id="a0535-114">Access 限制規則名稱</span><span class="sxs-lookup"><span data-stu-id="a0535-114">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0535-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0535-115">-PassThru</span></span>
<span data-ttu-id="a0535-116">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="a0535-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="a0535-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0535-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0535-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a0535-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a0535-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="a0535-119">-SlotName</span></span>
<span data-ttu-id="a0535-120">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="a0535-120">Deployment Slot Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0535-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="a0535-121">-TargetScmSite</span></span>
<span data-ttu-id="a0535-122">規則主要針對主網站或 Scm 網站。</span><span class="sxs-lookup"><span data-stu-id="a0535-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="a0535-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a0535-123">-WebAppName</span></span>
<span data-ttu-id="a0535-124">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0535-124">The name of the web app.</span></span>

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

### <span data-ttu-id="a0535-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a0535-125">-Confirm</span></span>
<span data-ttu-id="a0535-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0535-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0535-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0535-127">-WhatIf</span></span>
<span data-ttu-id="a0535-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0535-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0535-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0535-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0535-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0535-130">CommonParameters</span></span>
<span data-ttu-id="a0535-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0535-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0535-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0535-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0535-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a0535-133">INPUTS</span></span>

### <span data-ttu-id="a0535-134">System.object</span><span class="sxs-lookup"><span data-stu-id="a0535-134">System.String</span></span>

## <span data-ttu-id="a0535-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a0535-135">OUTPUTS</span></span>

### <span data-ttu-id="a0535-136">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a0535-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="a0535-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a0535-137">NOTES</span></span>

## <span data-ttu-id="a0535-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0535-138">RELATED LINKS</span></span>

[<span data-ttu-id="a0535-139">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a0535-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a0535-140">更新-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a0535-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a0535-141">附加 AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a0535-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
