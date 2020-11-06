---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 91cd7855b832a406fdd3ce9a959135936ee3c284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454948"
---
# <span data-ttu-id="e723b-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="e723b-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="e723b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e723b-102">SYNOPSIS</span></span>
<span data-ttu-id="e723b-103">透過建立目前設定的認可來儲存變更。</span><span class="sxs-lookup"><span data-stu-id="e723b-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e723b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e723b-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e723b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e723b-105">DESCRIPTION</span></span>
<span data-ttu-id="e723b-106">AzureRmApiManagementTenantGitConfiguration Cmdlet 會建立包含目前配置快照至知識庫中分支的認可，以 **儲存** 變更。</span><span class="sxs-lookup"><span data-stu-id="e723b-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="e723b-107">示例</span><span class="sxs-lookup"><span data-stu-id="e723b-107">EXAMPLES</span></span>

### <span data-ttu-id="e723b-108">範例1：儲存配置變更</span><span class="sxs-lookup"><span data-stu-id="e723b-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="e723b-109">這個命令會透過建立具有目前配置快照的認可來儲存變更至存儲庫中的指定分支。</span><span class="sxs-lookup"><span data-stu-id="e723b-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="e723b-110">參數</span><span class="sxs-lookup"><span data-stu-id="e723b-110">PARAMETERS</span></span>

### <span data-ttu-id="e723b-111">-分支</span><span class="sxs-lookup"><span data-stu-id="e723b-111">-Branch</span></span>
<span data-ttu-id="e723b-112">指定要在其中提交目前配置快照的 Git 分支的名稱。</span><span class="sxs-lookup"><span data-stu-id="e723b-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="e723b-113">-內容</span><span class="sxs-lookup"><span data-stu-id="e723b-113">-Context</span></span>
<span data-ttu-id="e723b-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e723b-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e723b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e723b-115">-Force</span></span>
<span data-ttu-id="e723b-116">指定此 Cmdlet 會將目前的設定資料庫提交到 Git 儲存庫，即使 Git 儲存庫中有覆蓋的更新變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="e723b-116">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="e723b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e723b-117">-PassThru</span></span>
<span data-ttu-id="e723b-118">指示這個 Cmdlet 會傳回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="e723b-118">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="e723b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e723b-119">-Confirm</span></span>
<span data-ttu-id="e723b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e723b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e723b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e723b-121">-WhatIf</span></span>
<span data-ttu-id="e723b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e723b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e723b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e723b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e723b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e723b-124">-DefaultProfile</span></span>
<span data-ttu-id="e723b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e723b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e723b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e723b-126">CommonParameters</span></span>
<span data-ttu-id="e723b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e723b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e723b-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e723b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e723b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e723b-129">INPUTS</span></span>

## <span data-ttu-id="e723b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e723b-130">OUTPUTS</span></span>

### <span data-ttu-id="e723b-131">ServiceManagement. PsApiManagementOperationResult （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e723b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="e723b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e723b-132">NOTES</span></span>

## <span data-ttu-id="e723b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e723b-133">RELATED LINKS</span></span>

[<span data-ttu-id="e723b-134">發佈-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="e723b-134">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


