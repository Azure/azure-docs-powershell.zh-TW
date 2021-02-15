---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142337"
---
# <span data-ttu-id="445d9-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="445d9-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="445d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="445d9-102">SYNOPSIS</span></span>
<span data-ttu-id="445d9-103">更新針對 Azure Web App 的主網站存取 Restiction config 至 SCM 網站的繼承。</span><span class="sxs-lookup"><span data-stu-id="445d9-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="445d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="445d9-104">SYNTAX</span></span>

### <span data-ttu-id="445d9-105">InputValuesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="445d9-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445d9-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="445d9-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445d9-107">說明</span><span class="sxs-lookup"><span data-stu-id="445d9-107">DESCRIPTION</span></span>
<span data-ttu-id="445d9-108">**AzWebAppAccessRestrictionConfig** Cmdlet 會更新 Azure Web App 的存取限制配置。</span><span class="sxs-lookup"><span data-stu-id="445d9-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="445d9-109">示例</span><span class="sxs-lookup"><span data-stu-id="445d9-109">EXAMPLES</span></span>

### <span data-ttu-id="445d9-110">範例1：更新 Web 應用程式 SCM 網站以使用主網站的存取限制</span><span class="sxs-lookup"><span data-stu-id="445d9-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="445d9-111">下列範例會更新屬於資源群組 MyResourceGroup 的 Web App，以在 scm 網站上使用主網站的存取限制配置。</span><span class="sxs-lookup"><span data-stu-id="445d9-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="445d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="445d9-112">PARAMETERS</span></span>

### <span data-ttu-id="445d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445d9-113">-DefaultProfile</span></span>
<span data-ttu-id="445d9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="445d9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="445d9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="445d9-115">-InputObject</span></span>
<span data-ttu-id="445d9-116">存取限制設定物件</span><span class="sxs-lookup"><span data-stu-id="445d9-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445d9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="445d9-117">-Name</span></span>
<span data-ttu-id="445d9-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="445d9-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="445d9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="445d9-119">-PassThru</span></span>
<span data-ttu-id="445d9-120">傳回 [存取限制] 設定物件。</span><span class="sxs-lookup"><span data-stu-id="445d9-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="445d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="445d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="445d9-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="445d9-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="445d9-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="445d9-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="445d9-124">Scm 網站會繼承主網站上設定的規則。</span><span class="sxs-lookup"><span data-stu-id="445d9-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445d9-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="445d9-125">-SlotName</span></span>
<span data-ttu-id="445d9-126">部署槽名稱。</span><span class="sxs-lookup"><span data-stu-id="445d9-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445d9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="445d9-127">-Confirm</span></span>
<span data-ttu-id="445d9-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="445d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445d9-129">-WhatIf</span></span>
<span data-ttu-id="445d9-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="445d9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="445d9-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="445d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445d9-132">CommonParameters</span></span>
<span data-ttu-id="445d9-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="445d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445d9-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="445d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445d9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="445d9-135">INPUTS</span></span>

### <span data-ttu-id="445d9-136">System.object</span><span class="sxs-lookup"><span data-stu-id="445d9-136">System.String</span></span>

### <span data-ttu-id="445d9-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="445d9-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="445d9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="445d9-138">OUTPUTS</span></span>

### <span data-ttu-id="445d9-139">PSAccessRestrictionConfig 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="445d9-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="445d9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="445d9-140">NOTES</span></span>

## <span data-ttu-id="445d9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="445d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="445d9-142">AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="445d9-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="445d9-143">附加 AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="445d9-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="445d9-144">移除-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="445d9-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
