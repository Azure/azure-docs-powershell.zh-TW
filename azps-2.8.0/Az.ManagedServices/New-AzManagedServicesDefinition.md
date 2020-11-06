---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 8bcf260156584ddf7c8c2ac0ec347a59214f20c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611877"
---
# <span data-ttu-id="4c8f7-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="4c8f7-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="4c8f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c8f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8f7-103">建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="4c8f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c8f7-104">SYNTAX</span></span>

### <span data-ttu-id="4c8f7-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="4c8f7-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c8f7-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="4c8f7-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c8f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="4c8f7-107">DESCRIPTION</span></span>
<span data-ttu-id="4c8f7-108">建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="4c8f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="4c8f7-109">EXAMPLES</span></span>

### <span data-ttu-id="4c8f7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4c8f7-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="4c8f7-111">根據所需的參數建立或更新註冊定義。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="4c8f7-112">範例2</span><span class="sxs-lookup"><span data-stu-id="4c8f7-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="4c8f7-113">使用 [方案詳細資料] 建立或更新登記定義。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="4c8f7-114">參數</span><span class="sxs-lookup"><span data-stu-id="4c8f7-114">PARAMETERS</span></span>

### <span data-ttu-id="4c8f7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c8f7-115">-AsJob</span></span>
<span data-ttu-id="4c8f7-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4c8f7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c8f7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8f7-117">-DefaultProfile</span></span>
<span data-ttu-id="4c8f7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c8f7-119">-描述</span><span class="sxs-lookup"><span data-stu-id="4c8f7-119">-Description</span></span>
<span data-ttu-id="4c8f7-120">註冊定義的描述。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="4c8f7-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="4c8f7-121">-ManagedByTenantId</span></span>
<span data-ttu-id="4c8f7-122">ManagedBy 租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-122">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="4c8f7-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="4c8f7-123">-PlanName</span></span>
<span data-ttu-id="4c8f7-124">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-124">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f7-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="4c8f7-125">-PlanProduct</span></span>
<span data-ttu-id="4c8f7-126">產品名稱。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-126">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f7-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4c8f7-127">-PlanPublisher</span></span>
<span data-ttu-id="4c8f7-128">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-128">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f7-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="4c8f7-129">-PlanVersion</span></span>
<span data-ttu-id="4c8f7-130">方案的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-130">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f7-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="4c8f7-131">-PrincipalId</span></span>
<span data-ttu-id="4c8f7-132">ManagedBy 主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-132">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="4c8f7-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="4c8f7-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="4c8f7-134">註冊定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-134">The name of the Registration Definition.</span></span>

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

### <span data-ttu-id="4c8f7-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4c8f7-135">-RoleDefinitionId</span></span>
<span data-ttu-id="4c8f7-136">受管理服務提供者的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-136">The Managed Service Provider's Role Identifier.</span></span>

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

### <span data-ttu-id="4c8f7-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4c8f7-137">-Confirm</span></span>
<span data-ttu-id="4c8f7-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c8f7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c8f7-139">-WhatIf</span></span>
<span data-ttu-id="4c8f7-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c8f7-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c8f7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8f7-142">CommonParameters</span></span>
<span data-ttu-id="4c8f7-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8f7-144">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c8f7-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8f7-145">輸入</span><span class="sxs-lookup"><span data-stu-id="4c8f7-145">INPUTS</span></span>

### <span data-ttu-id="4c8f7-146">所有</span><span class="sxs-lookup"><span data-stu-id="4c8f7-146">None</span></span>

## <span data-ttu-id="4c8f7-147">輸出</span><span class="sxs-lookup"><span data-stu-id="4c8f7-147">OUTPUTS</span></span>

### <span data-ttu-id="4c8f7-148">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="4c8f7-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="4c8f7-149">筆記</span><span class="sxs-lookup"><span data-stu-id="4c8f7-149">NOTES</span></span>

## <span data-ttu-id="4c8f7-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c8f7-150">RELATED LINKS</span></span>
