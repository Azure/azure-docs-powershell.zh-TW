---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916798"
---
# <span data-ttu-id="90f68-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90f68-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="90f68-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90f68-102">SYNOPSIS</span></span>
<span data-ttu-id="90f68-103">更新 Azure Web App 的主要網站 Access Restiction config 繼承至 SCM 網站。</span><span class="sxs-lookup"><span data-stu-id="90f68-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="90f68-104">語法</span><span class="sxs-lookup"><span data-stu-id="90f68-104">SYNTAX</span></span>

### <span data-ttu-id="90f68-105">InputValuesParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="90f68-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f68-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90f68-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f68-107">描述</span><span class="sxs-lookup"><span data-stu-id="90f68-107">DESCRIPTION</span></span>
<span data-ttu-id="90f68-108">**Update-AzWebAppAccessRestrictionConfig** Cmdlet 會更新 Azure Web App 的存取限制設定檔。</span><span class="sxs-lookup"><span data-stu-id="90f68-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="90f68-109">例子</span><span class="sxs-lookup"><span data-stu-id="90f68-109">EXAMPLES</span></span>

### <span data-ttu-id="90f68-110">範例 1：更新 Web App SCM 網站以使用主要網站的存取限制</span><span class="sxs-lookup"><span data-stu-id="90f68-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="90f68-111">下列範例更新名為 IpRule 的 Web App，此 App 屬於資源群組 MyResourceGroup，以使用 scm 網站上主網站的存取限制設定檔。</span><span class="sxs-lookup"><span data-stu-id="90f68-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="90f68-112">參數</span><span class="sxs-lookup"><span data-stu-id="90f68-112">PARAMETERS</span></span>

### <span data-ttu-id="90f68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f68-113">-DefaultProfile</span></span>
<span data-ttu-id="90f68-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90f68-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90f68-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90f68-115">-InputObject</span></span>
<span data-ttu-id="90f68-116">存取限制設定檔物件</span><span class="sxs-lookup"><span data-stu-id="90f68-116">The access restriction config object</span></span>

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

### <span data-ttu-id="90f68-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="90f68-117">-Name</span></span>
<span data-ttu-id="90f68-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="90f68-118">WebApp Name</span></span>

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

### <span data-ttu-id="90f68-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90f68-119">-PassThru</span></span>
<span data-ttu-id="90f68-120">返回存取限制 config 物件。</span><span class="sxs-lookup"><span data-stu-id="90f68-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="90f68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f68-121">-ResourceGroupName</span></span>
<span data-ttu-id="90f68-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="90f68-122">Resource Group Name</span></span>

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

### <span data-ttu-id="90f68-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90f68-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="90f68-124">Scm 網站會繼承主要網站上設定的規則。</span><span class="sxs-lookup"><span data-stu-id="90f68-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="90f68-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="90f68-125">-SlotName</span></span>
<span data-ttu-id="90f68-126">部署插槽名稱。</span><span class="sxs-lookup"><span data-stu-id="90f68-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="90f68-127">-確認</span><span class="sxs-lookup"><span data-stu-id="90f68-127">-Confirm</span></span>
<span data-ttu-id="90f68-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90f68-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f68-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f68-129">-WhatIf</span></span>
<span data-ttu-id="90f68-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90f68-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90f68-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90f68-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f68-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f68-132">CommonParameters</span></span>
<span data-ttu-id="90f68-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90f68-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f68-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90f68-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f68-135">輸入</span><span class="sxs-lookup"><span data-stu-id="90f68-135">INPUTS</span></span>

### <span data-ttu-id="90f68-136">System.String</span><span class="sxs-lookup"><span data-stu-id="90f68-136">System.String</span></span>

### <span data-ttu-id="90f68-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90f68-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90f68-138">輸出</span><span class="sxs-lookup"><span data-stu-id="90f68-138">OUTPUTS</span></span>

### <span data-ttu-id="90f68-139">Microsoft.Azure.Commands.WebApps.models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90f68-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="90f68-140">筆記</span><span class="sxs-lookup"><span data-stu-id="90f68-140">NOTES</span></span>

## <span data-ttu-id="90f68-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="90f68-141">RELATED LINKS</span></span>

[<span data-ttu-id="90f68-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="90f68-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="90f68-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="90f68-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="90f68-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="90f68-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
