---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 5c7e9d80ffd9109cda1f13f74b1febb3b28e10ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915890"
---
# <span data-ttu-id="28e93-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="28e93-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="28e93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28e93-102">SYNOPSIS</span></span>
<span data-ttu-id="28e93-103">更新 Azure 資訊安全中心的安全性設定</span><span class="sxs-lookup"><span data-stu-id="28e93-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="28e93-104">語法</span><span class="sxs-lookup"><span data-stu-id="28e93-104">SYNTAX</span></span>

### <span data-ttu-id="28e93-105">GeneralScope (預設) </span><span class="sxs-lookup"><span data-stu-id="28e93-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28e93-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="28e93-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28e93-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="28e93-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28e93-108">描述</span><span class="sxs-lookup"><span data-stu-id="28e93-108">DESCRIPTION</span></span>
<span data-ttu-id="28e93-109">此Set-AzSecuritySetting Cmdlet 會更新 Azure 資訊安全中心中的特定安全性設定。</span><span class="sxs-lookup"><span data-stu-id="28e93-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="28e93-110">例子</span><span class="sxs-lookup"><span data-stu-id="28e93-110">EXAMPLES</span></span>

### <span data-ttu-id="28e93-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="28e93-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="28e93-112">更新 MCAS 資料匯出設定</span><span class="sxs-lookup"><span data-stu-id="28e93-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="28e93-113">參數</span><span class="sxs-lookup"><span data-stu-id="28e93-113">PARAMETERS</span></span>

### <span data-ttu-id="28e93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e93-114">-DefaultProfile</span></span>
<span data-ttu-id="28e93-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28e93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28e93-116">-已啟用</span><span class="sxs-lookup"><span data-stu-id="28e93-116">-Enabled</span></span>
<span data-ttu-id="28e93-117">啟用設定。</span><span class="sxs-lookup"><span data-stu-id="28e93-117">Enables the setting.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e93-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28e93-118">-InputObject</span></span>
<span data-ttu-id="28e93-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="28e93-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28e93-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="28e93-120">-SettingKind</span></span>
<span data-ttu-id="28e93-121">設定種類。</span><span class="sxs-lookup"><span data-stu-id="28e93-121">Setting kind.</span></span> <span data-ttu-id="28e93-122"> (DataExportSettings) </span><span class="sxs-lookup"><span data-stu-id="28e93-122">(DataExportSettings)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e93-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="28e93-123">-SettingName</span></span>
<span data-ttu-id="28e93-124">設定名稱。</span><span class="sxs-lookup"><span data-stu-id="28e93-124">Setting name.</span></span> <span data-ttu-id="28e93-125"> (MCAS/WDATP) </span><span class="sxs-lookup"><span data-stu-id="28e93-125">(MCAS/WDATP)</span></span>

```yaml
Type: System.String
Parameter Sets: DataExportSettingsScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e93-126">-確認</span><span class="sxs-lookup"><span data-stu-id="28e93-126">-Confirm</span></span>
<span data-ttu-id="28e93-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28e93-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28e93-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28e93-128">-WhatIf</span></span>
<span data-ttu-id="28e93-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28e93-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28e93-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e93-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28e93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e93-131">CommonParameters</span></span>
<span data-ttu-id="28e93-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28e93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e93-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28e93-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e93-134">輸入</span><span class="sxs-lookup"><span data-stu-id="28e93-134">INPUTS</span></span>

### <span data-ttu-id="28e93-135">System.String</span><span class="sxs-lookup"><span data-stu-id="28e93-135">System.String</span></span>
### <span data-ttu-id="28e93-136">Microsoft.Azure.Commands.security.models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="28e93-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="28e93-137">Microsoft.Azure.Commands.security.models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="28e93-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="28e93-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28e93-138">System.Boolean</span></span>

## <span data-ttu-id="28e93-139">輸出</span><span class="sxs-lookup"><span data-stu-id="28e93-139">OUTPUTS</span></span>

### <span data-ttu-id="28e93-140">Microsoft.Azure.Commands.security.models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="28e93-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="28e93-141">Microsoft.Azure.Commands.security.models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="28e93-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="28e93-142">筆記</span><span class="sxs-lookup"><span data-stu-id="28e93-142">NOTES</span></span>

## <span data-ttu-id="28e93-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="28e93-143">RELATED LINKS</span></span>
