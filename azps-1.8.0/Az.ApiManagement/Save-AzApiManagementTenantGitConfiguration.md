---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b4abd2d8dab9e4c41d2e42be77bee62428ccc712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788801"
---
# <span data-ttu-id="ac223-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac223-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="ac223-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac223-102">SYNOPSIS</span></span>
<span data-ttu-id="ac223-103">透過建立目前設定的認可來儲存變更。</span><span class="sxs-lookup"><span data-stu-id="ac223-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="ac223-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac223-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac223-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac223-105">DESCRIPTION</span></span>
<span data-ttu-id="ac223-106">AzApiManagementTenantGitConfiguration Cmdlet 會建立包含目前配置快照至知識庫中分支的認可，以 **儲存** 變更。</span><span class="sxs-lookup"><span data-stu-id="ac223-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="ac223-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac223-107">EXAMPLES</span></span>

### <span data-ttu-id="ac223-108">範例1：儲存配置變更</span><span class="sxs-lookup"><span data-stu-id="ac223-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="ac223-109">這個命令會透過建立具有目前配置快照的認可來儲存變更至存儲庫中的指定分支。</span><span class="sxs-lookup"><span data-stu-id="ac223-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="ac223-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac223-110">PARAMETERS</span></span>

### <span data-ttu-id="ac223-111">-分支</span><span class="sxs-lookup"><span data-stu-id="ac223-111">-Branch</span></span>
<span data-ttu-id="ac223-112">指定要在其中提交目前配置快照的 Git 分支的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac223-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="ac223-113">-內容</span><span class="sxs-lookup"><span data-stu-id="ac223-113">-Context</span></span>
<span data-ttu-id="ac223-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="ac223-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ac223-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac223-115">-DefaultProfile</span></span>
<span data-ttu-id="ac223-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac223-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac223-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ac223-117">-Force</span></span>
<span data-ttu-id="ac223-118">指定此 Cmdlet 會將目前的設定資料庫提交到 Git 儲存庫，即使 Git 儲存庫中有覆蓋的更新變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="ac223-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="ac223-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac223-119">-PassThru</span></span>
<span data-ttu-id="ac223-120">指示這個 Cmdlet 會傳回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="ac223-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="ac223-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ac223-121">-Confirm</span></span>
<span data-ttu-id="ac223-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac223-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac223-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac223-123">-WhatIf</span></span>
<span data-ttu-id="ac223-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac223-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac223-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac223-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac223-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac223-126">CommonParameters</span></span>
<span data-ttu-id="ac223-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac223-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac223-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac223-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac223-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ac223-129">INPUTS</span></span>

### <span data-ttu-id="ac223-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ac223-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac223-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ac223-131">System.String</span></span>

### <span data-ttu-id="ac223-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ac223-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac223-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ac223-133">OUTPUTS</span></span>

### <span data-ttu-id="ac223-134">ServiceManagement. PsApiManagementOperationResult （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ac223-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="ac223-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ac223-135">NOTES</span></span>

## <span data-ttu-id="ac223-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac223-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac223-137">發佈-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac223-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


