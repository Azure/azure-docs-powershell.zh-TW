---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 2a867109bf44cd652eaf1d256d963796e06762cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446896"
---
# <span data-ttu-id="459f3-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="459f3-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="459f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="459f3-102">SYNOPSIS</span></span>
<span data-ttu-id="459f3-103">從 Git 分支發佈變更到設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="459f3-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="459f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="459f3-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="459f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="459f3-105">DESCRIPTION</span></span>
<span data-ttu-id="459f3-106">**AzureRmApiManagementTenantGitConfiguration** Cmdlet 會將來自 Git 分支的變更發佈到設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="459f3-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="459f3-107">您也可以在不發佈的情況下驗證 Git 分支中的變更。</span><span class="sxs-lookup"><span data-stu-id="459f3-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="459f3-108">示例</span><span class="sxs-lookup"><span data-stu-id="459f3-108">EXAMPLES</span></span>

### <span data-ttu-id="459f3-109">範例1：部署 Git 變更</span><span class="sxs-lookup"><span data-stu-id="459f3-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="459f3-110">這個命令會將指定分支的變更發佈到設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="459f3-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="459f3-111">範例2：驗證 Git 變更</span><span class="sxs-lookup"><span data-stu-id="459f3-111">Example 2: Validate Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="459f3-112">這個命令會驗證 Git 分支針對設定資料庫所做的變更。</span><span class="sxs-lookup"><span data-stu-id="459f3-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="459f3-113">它不會發佈變更。</span><span class="sxs-lookup"><span data-stu-id="459f3-113">It does not publish changes.</span></span>

## <span data-ttu-id="459f3-114">參數</span><span class="sxs-lookup"><span data-stu-id="459f3-114">PARAMETERS</span></span>

### <span data-ttu-id="459f3-115">-分支</span><span class="sxs-lookup"><span data-stu-id="459f3-115">-Branch</span></span>
<span data-ttu-id="459f3-116">指定此 Cmdlet 將配置部署到設定資料庫的 Git 分支的名稱。</span><span class="sxs-lookup"><span data-stu-id="459f3-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="459f3-117">-內容</span><span class="sxs-lookup"><span data-stu-id="459f3-117">-Context</span></span>
<span data-ttu-id="459f3-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="459f3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="459f3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="459f3-119">-Force</span></span>
<span data-ttu-id="459f3-120">表示此 Cmdlet 會刪除此更新中已刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="459f3-120">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="459f3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="459f3-121">-PassThru</span></span>
<span data-ttu-id="459f3-122">指示這個 Cmdlet 會傳回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="459f3-122">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="459f3-123">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="459f3-123">-ValidateOnly</span></span>
<span data-ttu-id="459f3-124">表示此 Cmdlet 會驗證指定 Git 分支中的變更。</span><span class="sxs-lookup"><span data-stu-id="459f3-124">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="459f3-125">它不會發佈至 [設定資料庫]。</span><span class="sxs-lookup"><span data-stu-id="459f3-125">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="459f3-126">-確認</span><span class="sxs-lookup"><span data-stu-id="459f3-126">-Confirm</span></span>
<span data-ttu-id="459f3-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="459f3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="459f3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="459f3-128">-WhatIf</span></span>
<span data-ttu-id="459f3-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="459f3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="459f3-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="459f3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="459f3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459f3-131">-DefaultProfile</span></span>
<span data-ttu-id="459f3-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="459f3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="459f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459f3-133">CommonParameters</span></span>
<span data-ttu-id="459f3-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="459f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459f3-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="459f3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459f3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="459f3-136">INPUTS</span></span>

## <span data-ttu-id="459f3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="459f3-137">OUTPUTS</span></span>

### <span data-ttu-id="459f3-138">ServiceManagement. PsApiManagementOperationResult （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="459f3-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="459f3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="459f3-139">NOTES</span></span>

## <span data-ttu-id="459f3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="459f3-140">RELATED LINKS</span></span>

[<span data-ttu-id="459f3-141">儲存-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="459f3-141">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


