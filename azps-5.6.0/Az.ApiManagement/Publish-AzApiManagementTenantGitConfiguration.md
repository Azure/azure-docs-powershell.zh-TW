---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b97a8502ff692911812c37d7f1af9d1ce1b33dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903709"
---
# <span data-ttu-id="56201-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="56201-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="56201-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56201-102">SYNOPSIS</span></span>
<span data-ttu-id="56201-103">將 Git 分支的變更發佈至組組資料庫。</span><span class="sxs-lookup"><span data-stu-id="56201-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="56201-104">語法</span><span class="sxs-lookup"><span data-stu-id="56201-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56201-105">描述</span><span class="sxs-lookup"><span data-stu-id="56201-105">DESCRIPTION</span></span>
<span data-ttu-id="56201-106">**Publish-AzApiManagementTenant GitConfiguration** Cmdlet 會發佈從 Git 分支到組組資料庫的變更。</span><span class="sxs-lookup"><span data-stu-id="56201-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="56201-107">您也可以在 Git 分支中驗證變更，而不發佈。</span><span class="sxs-lookup"><span data-stu-id="56201-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="56201-108">例子</span><span class="sxs-lookup"><span data-stu-id="56201-108">EXAMPLES</span></span>

### <span data-ttu-id="56201-109">範例 1：部署 Git 變更</span><span class="sxs-lookup"><span data-stu-id="56201-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="56201-110">此命令會發佈從指定分支到組組資料庫的變更。</span><span class="sxs-lookup"><span data-stu-id="56201-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="56201-111">範例 2：驗證 Git 變更</span><span class="sxs-lookup"><span data-stu-id="56201-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="56201-112">此命令會針對組組資料庫驗證 Git 分支中的變更。</span><span class="sxs-lookup"><span data-stu-id="56201-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="56201-113">它不會發佈變更。</span><span class="sxs-lookup"><span data-stu-id="56201-113">It does not publish changes.</span></span>

## <span data-ttu-id="56201-114">參數</span><span class="sxs-lookup"><span data-stu-id="56201-114">PARAMETERS</span></span>

### <span data-ttu-id="56201-115">-分支</span><span class="sxs-lookup"><span data-stu-id="56201-115">-Branch</span></span>
<span data-ttu-id="56201-116">指定此 Cmdlet 將群組原則部署到群組原則資料庫的 Git 分支名稱。</span><span class="sxs-lookup"><span data-stu-id="56201-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="56201-117">-內容</span><span class="sxs-lookup"><span data-stu-id="56201-117">-Context</span></span>
<span data-ttu-id="56201-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="56201-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56201-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56201-119">-DefaultProfile</span></span>
<span data-ttu-id="56201-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56201-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56201-121">-強制</span><span class="sxs-lookup"><span data-stu-id="56201-121">-Force</span></span>
<span data-ttu-id="56201-122">表示此 Cmdlet 會刪除此更新中已刪除之產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="56201-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56201-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56201-123">-PassThru</span></span>
<span data-ttu-id="56201-124">表示此 Cmdlet 會返回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="56201-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56201-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="56201-125">-ValidateOnly</span></span>
<span data-ttu-id="56201-126">表示此 Cmdlet 會驗證指定 Git 分支中的變更。</span><span class="sxs-lookup"><span data-stu-id="56201-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="56201-127">它不會發佈到組組資料庫。</span><span class="sxs-lookup"><span data-stu-id="56201-127">It does not publish to the configuration database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56201-128">-確認</span><span class="sxs-lookup"><span data-stu-id="56201-128">-Confirm</span></span>
<span data-ttu-id="56201-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56201-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56201-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56201-130">-WhatIf</span></span>
<span data-ttu-id="56201-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56201-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56201-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56201-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56201-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56201-133">CommonParameters</span></span>
<span data-ttu-id="56201-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56201-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56201-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56201-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56201-136">輸入</span><span class="sxs-lookup"><span data-stu-id="56201-136">INPUTS</span></span>

### <span data-ttu-id="56201-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="56201-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56201-138">System.String</span><span class="sxs-lookup"><span data-stu-id="56201-138">System.String</span></span>

### <span data-ttu-id="56201-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56201-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56201-140">輸出</span><span class="sxs-lookup"><span data-stu-id="56201-140">OUTPUTS</span></span>

### <span data-ttu-id="56201-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="56201-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="56201-142">筆記</span><span class="sxs-lookup"><span data-stu-id="56201-142">NOTES</span></span>

## <span data-ttu-id="56201-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="56201-143">RELATED LINKS</span></span>

[<span data-ttu-id="56201-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="56201-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


