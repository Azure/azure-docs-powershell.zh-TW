---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecuritySetting.md
ms.openlocfilehash: 09273ee53eb3e4ced7249505e73f4f9f39db5291
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130794"
---
# <span data-ttu-id="46a63-101">Set-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="46a63-101">Set-AzSecuritySetting</span></span>

## <span data-ttu-id="46a63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46a63-102">SYNOPSIS</span></span>
<span data-ttu-id="46a63-103">更新 Azure 安全中心中的安全性設定</span><span class="sxs-lookup"><span data-stu-id="46a63-103">Update a security setting in Azure Security Center</span></span>

## <span data-ttu-id="46a63-104">句法</span><span class="sxs-lookup"><span data-stu-id="46a63-104">SYNTAX</span></span>

### <span data-ttu-id="46a63-105">GeneralScope (預設) </span><span class="sxs-lookup"><span data-stu-id="46a63-105">GeneralScope (Default)</span></span>
```
Set-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a63-106">DataExportSettingsScope</span><span class="sxs-lookup"><span data-stu-id="46a63-106">DataExportSettingsScope</span></span>
```
Set-AzSecuritySetting -SettingName <String> -SettingKind <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a63-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="46a63-107">InputObject</span></span>
```
Set-AzSecuritySetting -InputObject <PSSecuritySetting> [-Enabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a63-108">說明</span><span class="sxs-lookup"><span data-stu-id="46a63-108">DESCRIPTION</span></span>
<span data-ttu-id="46a63-109">Set-AzSecuritySetting Cmdlet 會更新 Azure 安全中心中的特定安全性設定。</span><span class="sxs-lookup"><span data-stu-id="46a63-109">The Set-AzSecuritySetting cmdlet updates a specific security setting in Azure Security Center.</span></span>

## <span data-ttu-id="46a63-110">示例</span><span class="sxs-lookup"><span data-stu-id="46a63-110">EXAMPLES</span></span>

### <span data-ttu-id="46a63-111">範例1</span><span class="sxs-lookup"><span data-stu-id="46a63-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS" -SettingKind "DataExportSettings" -Enabled $true

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="46a63-112">更新 MCAS 資料匯出設定</span><span class="sxs-lookup"><span data-stu-id="46a63-112">Updates an MCAS data export setting</span></span>   

## <span data-ttu-id="46a63-113">參數</span><span class="sxs-lookup"><span data-stu-id="46a63-113">PARAMETERS</span></span>

### <span data-ttu-id="46a63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a63-114">-DefaultProfile</span></span>
<span data-ttu-id="46a63-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46a63-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a63-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="46a63-116">-Enabled</span></span>
<span data-ttu-id="46a63-117">啟用 [設定]。</span><span class="sxs-lookup"><span data-stu-id="46a63-117">Enables the setting.</span></span>

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

### <span data-ttu-id="46a63-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46a63-118">-InputObject</span></span>
<span data-ttu-id="46a63-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="46a63-119">Input Object.</span></span>

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

### <span data-ttu-id="46a63-120">-SettingKind</span><span class="sxs-lookup"><span data-stu-id="46a63-120">-SettingKind</span></span>
<span data-ttu-id="46a63-121">設定類型。</span><span class="sxs-lookup"><span data-stu-id="46a63-121">Setting kind.</span></span> <span data-ttu-id="46a63-122"> (DataExportSettings) </span><span class="sxs-lookup"><span data-stu-id="46a63-122">(DataExportSettings)</span></span>

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

### <span data-ttu-id="46a63-123">-SettingName</span><span class="sxs-lookup"><span data-stu-id="46a63-123">-SettingName</span></span>
<span data-ttu-id="46a63-124">設定名稱。</span><span class="sxs-lookup"><span data-stu-id="46a63-124">Setting name.</span></span> <span data-ttu-id="46a63-125"> (MCAS/WDATP) </span><span class="sxs-lookup"><span data-stu-id="46a63-125">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="46a63-126">-確認</span><span class="sxs-lookup"><span data-stu-id="46a63-126">-Confirm</span></span>
<span data-ttu-id="46a63-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="46a63-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a63-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a63-128">-WhatIf</span></span>
<span data-ttu-id="46a63-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46a63-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a63-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46a63-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a63-131">CommonParameters</span></span>
<span data-ttu-id="46a63-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46a63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a63-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="46a63-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a63-134">輸入</span><span class="sxs-lookup"><span data-stu-id="46a63-134">INPUTS</span></span>

### <span data-ttu-id="46a63-135">System.object</span><span class="sxs-lookup"><span data-stu-id="46a63-135">System.String</span></span>
### <span data-ttu-id="46a63-136">PSSecuritySetting （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="46a63-136">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="46a63-137">PSSecurityDataExportSetting （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="46a63-137">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

### <span data-ttu-id="46a63-138">System.object</span><span class="sxs-lookup"><span data-stu-id="46a63-138">System.Boolean</span></span>

## <span data-ttu-id="46a63-139">輸出</span><span class="sxs-lookup"><span data-stu-id="46a63-139">OUTPUTS</span></span>

### <span data-ttu-id="46a63-140">PSSecuritySetting （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="46a63-140">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="46a63-141">PSSecurityDataExportSetting （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="46a63-141">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="46a63-142">筆記</span><span class="sxs-lookup"><span data-stu-id="46a63-142">NOTES</span></span>

## <span data-ttu-id="46a63-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="46a63-143">RELATED LINKS</span></span>
