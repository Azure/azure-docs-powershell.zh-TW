---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456400"
---
# <span data-ttu-id="929fc-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="929fc-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="929fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="929fc-102">SYNOPSIS</span></span>
<span data-ttu-id="929fc-103">建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="929fc-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="929fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="929fc-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="929fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="929fc-105">DESCRIPTION</span></span>
<span data-ttu-id="929fc-106">**新的-AzureRmManagedApplicationDefinition** Cmdlet 會建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="929fc-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="929fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="929fc-107">EXAMPLES</span></span>

### <span data-ttu-id="929fc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="929fc-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="929fc-109">這個命令會建立受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="929fc-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="929fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="929fc-110">PARAMETERS</span></span>

### <span data-ttu-id="929fc-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="929fc-111">-ApiVersion</span></span>
<span data-ttu-id="929fc-112">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="929fc-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="929fc-113">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="929fc-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="929fc-114">-授權</span><span class="sxs-lookup"><span data-stu-id="929fc-114">-Authorization</span></span>
<span data-ttu-id="929fc-115">受管理的應用程式定義授權。</span><span class="sxs-lookup"><span data-stu-id="929fc-115">The managed application definition authorization.</span></span>
<span data-ttu-id="929fc-116">以逗號分隔授權對的格式 \<principalId\> ：\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="929fc-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929fc-117">-DefaultProfile</span></span>
<span data-ttu-id="929fc-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="929fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="929fc-119">-描述</span><span class="sxs-lookup"><span data-stu-id="929fc-119">-Description</span></span>
<span data-ttu-id="929fc-120">受管理的應用程式定義說明。</span><span class="sxs-lookup"><span data-stu-id="929fc-120">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="929fc-121">-DisplayName</span></span>
<span data-ttu-id="929fc-122">受管理的應用程式定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="929fc-122">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-123">-位置</span><span class="sxs-lookup"><span data-stu-id="929fc-123">-Location</span></span>
<span data-ttu-id="929fc-124">資源位置。</span><span class="sxs-lookup"><span data-stu-id="929fc-124">The resource location.</span></span>

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

### <span data-ttu-id="929fc-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="929fc-125">-LockLevel</span></span>
<span data-ttu-id="929fc-126">受管理的應用程式定義鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="929fc-126">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="929fc-127">-Name</span></span>
<span data-ttu-id="929fc-128">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="929fc-128">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="929fc-129">-PackageFileUri</span></span>
<span data-ttu-id="929fc-130">受管理的應用程式定義套件檔案 uri。</span><span class="sxs-lookup"><span data-stu-id="929fc-130">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-131">-預先</span><span class="sxs-lookup"><span data-stu-id="929fc-131">-Pre</span></span>
<span data-ttu-id="929fc-132">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="929fc-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="929fc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="929fc-133">-ResourceGroupName</span></span>
<span data-ttu-id="929fc-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="929fc-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="929fc-135">-Tag</span></span>
<span data-ttu-id="929fc-136">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="929fc-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-137">-確認</span><span class="sxs-lookup"><span data-stu-id="929fc-137">-Confirm</span></span>
<span data-ttu-id="929fc-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="929fc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="929fc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="929fc-139">-WhatIf</span></span>
<span data-ttu-id="929fc-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="929fc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="929fc-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="929fc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="929fc-142">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="929fc-142">-CreateUiDefinition</span></span>
<span data-ttu-id="929fc-143">受管理的應用程式定義會建立 ui 定義。</span><span class="sxs-lookup"><span data-stu-id="929fc-143">The managed application definition create ui definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="929fc-144">-MainTemplate</span></span>
<span data-ttu-id="929fc-145">受管理的應用程式定義主範本。</span><span class="sxs-lookup"><span data-stu-id="929fc-145">The managed application definition main template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="929fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929fc-146">CommonParameters</span></span>
<span data-ttu-id="929fc-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="929fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929fc-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="929fc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929fc-149">輸入</span><span class="sxs-lookup"><span data-stu-id="929fc-149">INPUTS</span></span>

### <span data-ttu-id="929fc-150">System.object</span><span class="sxs-lookup"><span data-stu-id="929fc-150">System.String</span></span>
<span data-ttu-id="929fc-151">ApplicationLockLevel [] System.object. Hashtable. 雜湊散集合.. 雜湊表</span><span class="sxs-lookup"><span data-stu-id="929fc-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="929fc-152">輸出</span><span class="sxs-lookup"><span data-stu-id="929fc-152">OUTPUTS</span></span>

### <span data-ttu-id="929fc-153">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="929fc-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="929fc-154">筆記</span><span class="sxs-lookup"><span data-stu-id="929fc-154">NOTES</span></span>

## <span data-ttu-id="929fc-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="929fc-155">RELATED LINKS</span></span>

