---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448787"
---
# <span data-ttu-id="47c04-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="47c04-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="47c04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47c04-102">SYNOPSIS</span></span>
<span data-ttu-id="47c04-103">從 Git 分支發佈變更到設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="47c04-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47c04-104">句法</span><span class="sxs-lookup"><span data-stu-id="47c04-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47c04-105">說明</span><span class="sxs-lookup"><span data-stu-id="47c04-105">DESCRIPTION</span></span>
<span data-ttu-id="47c04-106">**AzureRmApiManagementTenantGitConfiguration** Cmdlet 會將來自 Git 分支的變更發佈到設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="47c04-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="47c04-107">您也可以在不發佈的情況下驗證 Git 分支中的變更。</span><span class="sxs-lookup"><span data-stu-id="47c04-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="47c04-108">示例</span><span class="sxs-lookup"><span data-stu-id="47c04-108">EXAMPLES</span></span>

### <span data-ttu-id="47c04-109">範例1：部署 Git 變更</span><span class="sxs-lookup"><span data-stu-id="47c04-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="47c04-110">這個命令會將指定分支的變更發佈到設定資料庫。</span><span class="sxs-lookup"><span data-stu-id="47c04-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="47c04-111">範例2：驗證 Git 變更</span><span class="sxs-lookup"><span data-stu-id="47c04-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="47c04-112">這個命令會驗證 Git 分支針對設定資料庫所做的變更。</span><span class="sxs-lookup"><span data-stu-id="47c04-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="47c04-113">它不會發佈變更。</span><span class="sxs-lookup"><span data-stu-id="47c04-113">It does not publish changes.</span></span>

## <span data-ttu-id="47c04-114">參數</span><span class="sxs-lookup"><span data-stu-id="47c04-114">PARAMETERS</span></span>

### <span data-ttu-id="47c04-115">-分支</span><span class="sxs-lookup"><span data-stu-id="47c04-115">-Branch</span></span>
<span data-ttu-id="47c04-116">指定此 Cmdlet 將配置部署到設定資料庫的 Git 分支的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c04-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="47c04-117">-內容</span><span class="sxs-lookup"><span data-stu-id="47c04-117">-Context</span></span>
<span data-ttu-id="47c04-118">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="47c04-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c04-119">-DefaultProfile</span></span>
<span data-ttu-id="47c04-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47c04-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="47c04-121">-Force</span><span class="sxs-lookup"><span data-stu-id="47c04-121">-Force</span></span>
<span data-ttu-id="47c04-122">表示此 Cmdlet 會刪除此更新中已刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="47c04-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c04-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47c04-123">-PassThru</span></span>
<span data-ttu-id="47c04-124">指示這個 Cmdlet 會傳回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="47c04-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c04-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="47c04-125">-ValidateOnly</span></span>
<span data-ttu-id="47c04-126">表示此 Cmdlet 會驗證指定 Git 分支中的變更。</span><span class="sxs-lookup"><span data-stu-id="47c04-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="47c04-127">它不會發佈至 [設定資料庫]。</span><span class="sxs-lookup"><span data-stu-id="47c04-127">It does not publish to the configuration database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47c04-128">-確認</span><span class="sxs-lookup"><span data-stu-id="47c04-128">-Confirm</span></span>
<span data-ttu-id="47c04-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47c04-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c04-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47c04-130">-WhatIf</span></span>
<span data-ttu-id="47c04-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47c04-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47c04-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47c04-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47c04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c04-133">CommonParameters</span></span>
<span data-ttu-id="47c04-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47c04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c04-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47c04-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c04-136">輸入</span><span class="sxs-lookup"><span data-stu-id="47c04-136">INPUTS</span></span>

### <span data-ttu-id="47c04-137">所有</span><span class="sxs-lookup"><span data-stu-id="47c04-137">None</span></span>
<span data-ttu-id="47c04-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="47c04-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47c04-139">輸出</span><span class="sxs-lookup"><span data-stu-id="47c04-139">OUTPUTS</span></span>

### <span data-ttu-id="47c04-140">ServiceManagement. PsApiManagementOperationResult （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="47c04-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="47c04-141">筆記</span><span class="sxs-lookup"><span data-stu-id="47c04-141">NOTES</span></span>

## <span data-ttu-id="47c04-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="47c04-142">RELATED LINKS</span></span>

[<span data-ttu-id="47c04-143">儲存-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="47c04-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


