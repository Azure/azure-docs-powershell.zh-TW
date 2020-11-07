---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 278c80206e1221550afc5c603c618c8219ea152f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792377"
---
# <span data-ttu-id="b436f-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b436f-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="b436f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b436f-102">SYNOPSIS</span></span>
<span data-ttu-id="b436f-103">在受管理的實例上啟用 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="b436f-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="b436f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b436f-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b436f-105">說明</span><span class="sxs-lookup"><span data-stu-id="b436f-105">DESCRIPTION</span></span>
<span data-ttu-id="b436f-106">**Enable-AzSqlInstanceAdvancedDataSecurity** Cmdlet 可在受管理的實例上啟用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="b436f-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="b436f-107">[高級資料安全性] 是一個整合的安全性套件，其中包含受管理實例的資料分類、漏洞評估及高級威脅防護。</span><span class="sxs-lookup"><span data-stu-id="b436f-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="b436f-108"> (會自動建立新的儲存空間帳戶來儲存漏洞評量。</span><span class="sxs-lookup"><span data-stu-id="b436f-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="b436f-109">如果先前已針對此目的建立儲存空間帳戶，則會改為使用它) </span><span class="sxs-lookup"><span data-stu-id="b436f-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="b436f-110">示例</span><span class="sxs-lookup"><span data-stu-id="b436f-110">EXAMPLES</span></span>

### <span data-ttu-id="b436f-111">範例 1-啟用受管理實例的高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="b436f-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="b436f-112">範例 2-從伺服器資源啟用 managed 實例高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="b436f-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="b436f-113">參數</span><span class="sxs-lookup"><span data-stu-id="b436f-113">PARAMETERS</span></span>

### <span data-ttu-id="b436f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b436f-114">-AsJob</span></span>
<span data-ttu-id="b436f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b436f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b436f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b436f-116">-DefaultProfile</span></span>
<span data-ttu-id="b436f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b436f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b436f-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b436f-118">-DeploymentName</span></span>
<span data-ttu-id="b436f-119">為高級資料安全性部署提供自訂名稱</span><span class="sxs-lookup"><span data-stu-id="b436f-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="b436f-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="b436f-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="b436f-121">請勿自動啟用漏洞評估 (這將不會建立儲存空間帳戶) </span><span class="sxs-lookup"><span data-stu-id="b436f-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="b436f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b436f-122">-InputObject</span></span>
<span data-ttu-id="b436f-123">要與高級資料安全性原則作業搭配使用的 managed 實例物件</span><span class="sxs-lookup"><span data-stu-id="b436f-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b436f-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b436f-124">-InstanceName</span></span>
<span data-ttu-id="b436f-125">SQL 資料庫管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="b436f-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="b436f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b436f-126">-ResourceGroupName</span></span>
<span data-ttu-id="b436f-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b436f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="b436f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b436f-128">-Confirm</span></span>
<span data-ttu-id="b436f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b436f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b436f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b436f-130">-WhatIf</span></span>
<span data-ttu-id="b436f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b436f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b436f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b436f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b436f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b436f-133">CommonParameters</span></span>
<span data-ttu-id="b436f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b436f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b436f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b436f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b436f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b436f-136">INPUTS</span></span>

### <span data-ttu-id="b436f-137">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="b436f-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="b436f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b436f-138">System.String</span></span>

## <span data-ttu-id="b436f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b436f-139">OUTPUTS</span></span>

### <span data-ttu-id="b436f-140">ManagedInstanceAdvancedDataSecurityPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="b436f-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b436f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b436f-141">NOTES</span></span>

## <span data-ttu-id="b436f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b436f-142">RELATED LINKS</span></span>
