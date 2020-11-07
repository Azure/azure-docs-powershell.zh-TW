---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 36efc8b3dfec4bcc126191d68c04c2cd5d071fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957522"
---
# <span data-ttu-id="565b9-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="565b9-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="565b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="565b9-102">SYNOPSIS</span></span>
<span data-ttu-id="565b9-103">在伺服器上啟用 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="565b9-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="565b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="565b9-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="565b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="565b9-105">DESCRIPTION</span></span>
<span data-ttu-id="565b9-106">**Enable-AzSqlServerAdvancedDataSecurity** Cmdlet 可在伺服器上啟用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="565b9-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="565b9-107">[高級資料安全性] 是一個整合的安全性套件，其中包括您伺服器的資料分類、漏洞評估及高級威脅防護。</span><span class="sxs-lookup"><span data-stu-id="565b9-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="565b9-108"> (會自動建立新的儲存空間帳戶來儲存漏洞評量。</span><span class="sxs-lookup"><span data-stu-id="565b9-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="565b9-109">如果先前已針對此目的建立儲存空間帳戶，則會改為使用它) </span><span class="sxs-lookup"><span data-stu-id="565b9-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="565b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="565b9-110">EXAMPLES</span></span>

### <span data-ttu-id="565b9-111">範例 1-啟用伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="565b9-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="565b9-112">範例 2-從伺服器資源啟用伺服器高級資料安全性</span><span class="sxs-lookup"><span data-stu-id="565b9-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="565b9-113">參數</span><span class="sxs-lookup"><span data-stu-id="565b9-113">PARAMETERS</span></span>

### <span data-ttu-id="565b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="565b9-114">-AsJob</span></span>
<span data-ttu-id="565b9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="565b9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="565b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565b9-116">-DefaultProfile</span></span>
<span data-ttu-id="565b9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="565b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="565b9-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="565b9-118">-DeploymentName</span></span>
<span data-ttu-id="565b9-119">為高級資料安全性部署提供自訂名稱</span><span class="sxs-lookup"><span data-stu-id="565b9-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="565b9-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="565b9-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="565b9-121">請勿自動啟用漏洞評估 (這將不會建立儲存空間帳戶) </span><span class="sxs-lookup"><span data-stu-id="565b9-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="565b9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="565b9-122">-InputObject</span></span>
<span data-ttu-id="565b9-123">要搭配高級資料安全性原則作業使用的伺服器物件</span><span class="sxs-lookup"><span data-stu-id="565b9-123">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="565b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="565b9-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="565b9-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="565b9-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="565b9-126">-ServerName</span></span>
<span data-ttu-id="565b9-127">SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="565b9-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="565b9-128">-確認</span><span class="sxs-lookup"><span data-stu-id="565b9-128">-Confirm</span></span>
<span data-ttu-id="565b9-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="565b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="565b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="565b9-130">-WhatIf</span></span>
<span data-ttu-id="565b9-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="565b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="565b9-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="565b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="565b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565b9-133">CommonParameters</span></span>
<span data-ttu-id="565b9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="565b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565b9-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="565b9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565b9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="565b9-136">INPUTS</span></span>

### <span data-ttu-id="565b9-137">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="565b9-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="565b9-138">System.object</span><span class="sxs-lookup"><span data-stu-id="565b9-138">System.String</span></span>

## <span data-ttu-id="565b9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="565b9-139">OUTPUTS</span></span>

### <span data-ttu-id="565b9-140">ServerAdvancedDataSecurityPolicyModel 中的 [AdvancedThreatProtection]</span><span class="sxs-lookup"><span data-stu-id="565b9-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="565b9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="565b9-141">NOTES</span></span>

## <span data-ttu-id="565b9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="565b9-142">RELATED LINKS</span></span>
