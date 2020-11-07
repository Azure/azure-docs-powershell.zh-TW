---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 3451a922af2b2af469b7edba1539f52cabb64eb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801933"
---
# <span data-ttu-id="614c3-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="614c3-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="614c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="614c3-102">SYNOPSIS</span></span>
<span data-ttu-id="614c3-103">建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="614c3-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="614c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="614c3-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="614c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="614c3-105">DESCRIPTION</span></span>
<span data-ttu-id="614c3-106">**新的-AzureRmManagedApplicationDefinition** Cmdlet 會建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="614c3-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="614c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="614c3-107">EXAMPLES</span></span>

### <span data-ttu-id="614c3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="614c3-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="614c3-109">這個命令會建立受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="614c3-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="614c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="614c3-110">PARAMETERS</span></span>

### <span data-ttu-id="614c3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="614c3-111">-ApiVersion</span></span>
<span data-ttu-id="614c3-112">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="614c3-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="614c3-113">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="614c3-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-114">-授權</span><span class="sxs-lookup"><span data-stu-id="614c3-114">-Authorization</span></span>
<span data-ttu-id="614c3-115">受管理的應用程式定義授權。</span><span class="sxs-lookup"><span data-stu-id="614c3-115">The managed application definition authorization.</span></span>
<span data-ttu-id="614c3-116">以逗號分隔授權對的格式 \<principalId\> ：\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="614c3-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="614c3-117">-CreateUiDefinition</span></span>
<span data-ttu-id="614c3-118">受管理的應用程式定義建立使用者介面定義</span><span class="sxs-lookup"><span data-stu-id="614c3-118">The managed application definition create ui definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614c3-119">-DefaultProfile</span></span>
<span data-ttu-id="614c3-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="614c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-121">-描述</span><span class="sxs-lookup"><span data-stu-id="614c3-121">-Description</span></span>
<span data-ttu-id="614c3-122">受管理的應用程式定義說明。</span><span class="sxs-lookup"><span data-stu-id="614c3-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="614c3-123">-DisplayName</span></span>
<span data-ttu-id="614c3-124">受管理的應用程式定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="614c3-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-125">-位置</span><span class="sxs-lookup"><span data-stu-id="614c3-125">-Location</span></span>
<span data-ttu-id="614c3-126">資源位置。</span><span class="sxs-lookup"><span data-stu-id="614c3-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="614c3-127">-LockLevel</span></span>
<span data-ttu-id="614c3-128">受管理的應用程式定義鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="614c3-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="614c3-129">-MainTemplate</span></span>
<span data-ttu-id="614c3-130">受管理的應用程式定義主範本</span><span class="sxs-lookup"><span data-stu-id="614c3-130">The managed application definition main template</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="614c3-131">-Name</span></span>
<span data-ttu-id="614c3-132">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="614c3-132">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="614c3-133">-PackageFileUri</span></span>
<span data-ttu-id="614c3-134">受管理的應用程式定義套件檔案 uri。</span><span class="sxs-lookup"><span data-stu-id="614c3-134">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-135">-預先</span><span class="sxs-lookup"><span data-stu-id="614c3-135">-Pre</span></span>
<span data-ttu-id="614c3-136">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="614c3-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614c3-137">-ResourceGroupName</span></span>
<span data-ttu-id="614c3-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="614c3-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="614c3-139">-Tag</span></span>
<span data-ttu-id="614c3-140">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="614c3-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-141">-確認</span><span class="sxs-lookup"><span data-stu-id="614c3-141">-Confirm</span></span>
<span data-ttu-id="614c3-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="614c3-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="614c3-143">-WhatIf</span></span>
<span data-ttu-id="614c3-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="614c3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="614c3-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="614c3-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614c3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614c3-146">CommonParameters</span></span>
<span data-ttu-id="614c3-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="614c3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614c3-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="614c3-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614c3-149">輸入</span><span class="sxs-lookup"><span data-stu-id="614c3-149">INPUTS</span></span>

### <span data-ttu-id="614c3-150">System.object</span><span class="sxs-lookup"><span data-stu-id="614c3-150">System.String</span></span>
<span data-ttu-id="614c3-151">ApplicationLockLevel [] System.object. Hashtable. 雜湊散集合.. 雜湊表</span><span class="sxs-lookup"><span data-stu-id="614c3-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="614c3-152">輸出</span><span class="sxs-lookup"><span data-stu-id="614c3-152">OUTPUTS</span></span>

### <span data-ttu-id="614c3-153">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="614c3-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="614c3-154">筆記</span><span class="sxs-lookup"><span data-stu-id="614c3-154">NOTES</span></span>

## <span data-ttu-id="614c3-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="614c3-155">RELATED LINKS</span></span>
