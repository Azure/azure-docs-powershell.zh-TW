---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: eb865535fcb4ee49b834e923fcf3f319ff5de074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905302"
---
# <span data-ttu-id="56aa9-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="56aa9-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="56aa9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="56aa9-103">建立目前配置的提交以節省變更。</span><span class="sxs-lookup"><span data-stu-id="56aa9-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="56aa9-104">語法</span><span class="sxs-lookup"><span data-stu-id="56aa9-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56aa9-105">描述</span><span class="sxs-lookup"><span data-stu-id="56aa9-105">DESCRIPTION</span></span>
<span data-ttu-id="56aa9-106">**Save-AzApiManagementTenant GitConfiguration** Cmdlet 會建立包含存放庫中分支之目前組配置快照的確認，以儲存變更。</span><span class="sxs-lookup"><span data-stu-id="56aa9-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="56aa9-107">例子</span><span class="sxs-lookup"><span data-stu-id="56aa9-107">EXAMPLES</span></span>

### <span data-ttu-id="56aa9-108">範例 1：儲存組配置的變更</span><span class="sxs-lookup"><span data-stu-id="56aa9-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="56aa9-109">此命令會儲存變更，以建立存放庫中指定分支之目前組配置快照的提交。</span><span class="sxs-lookup"><span data-stu-id="56aa9-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="56aa9-110">參數</span><span class="sxs-lookup"><span data-stu-id="56aa9-110">PARAMETERS</span></span>

### <span data-ttu-id="56aa9-111">-分支</span><span class="sxs-lookup"><span data-stu-id="56aa9-111">-Branch</span></span>
<span data-ttu-id="56aa9-112">指定要提交目前群組原則快照的 Git 分支名稱。</span><span class="sxs-lookup"><span data-stu-id="56aa9-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="56aa9-113">-內容</span><span class="sxs-lookup"><span data-stu-id="56aa9-113">-Context</span></span>
<span data-ttu-id="56aa9-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="56aa9-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56aa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56aa9-115">-DefaultProfile</span></span>
<span data-ttu-id="56aa9-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56aa9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56aa9-117">-強制</span><span class="sxs-lookup"><span data-stu-id="56aa9-117">-Force</span></span>
<span data-ttu-id="56aa9-118">指定此 Cmdlet 會向 Git 存放庫提交目前的群組原則資料庫，即使 Git 存放庫有較新的變更已重寫。</span><span class="sxs-lookup"><span data-stu-id="56aa9-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="56aa9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56aa9-119">-PassThru</span></span>
<span data-ttu-id="56aa9-120">表示此 Cmdlet 會返回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="56aa9-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="56aa9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="56aa9-121">-Confirm</span></span>
<span data-ttu-id="56aa9-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56aa9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56aa9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56aa9-123">-WhatIf</span></span>
<span data-ttu-id="56aa9-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56aa9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56aa9-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56aa9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56aa9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56aa9-126">CommonParameters</span></span>
<span data-ttu-id="56aa9-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56aa9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56aa9-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56aa9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56aa9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="56aa9-129">INPUTS</span></span>

### <span data-ttu-id="56aa9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="56aa9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56aa9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="56aa9-131">System.String</span></span>

### <span data-ttu-id="56aa9-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56aa9-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56aa9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="56aa9-133">OUTPUTS</span></span>

### <span data-ttu-id="56aa9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="56aa9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="56aa9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="56aa9-135">NOTES</span></span>

## <span data-ttu-id="56aa9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="56aa9-136">RELATED LINKS</span></span>

[<span data-ttu-id="56aa9-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="56aa9-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


