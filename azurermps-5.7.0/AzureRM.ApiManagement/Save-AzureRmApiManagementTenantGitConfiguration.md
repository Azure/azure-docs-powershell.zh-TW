---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 7401c359a9af82d1b65749a3276aada89ab9320d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444803"
---
# <span data-ttu-id="94715-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="94715-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="94715-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94715-102">SYNOPSIS</span></span>
<span data-ttu-id="94715-103">透過建立目前設定的認可來儲存變更。</span><span class="sxs-lookup"><span data-stu-id="94715-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94715-104">句法</span><span class="sxs-lookup"><span data-stu-id="94715-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94715-105">說明</span><span class="sxs-lookup"><span data-stu-id="94715-105">DESCRIPTION</span></span>
<span data-ttu-id="94715-106">AzureRmApiManagementTenantGitConfiguration Cmdlet 會建立包含目前配置快照至知識庫中分支的認可，以 **儲存** 變更。</span><span class="sxs-lookup"><span data-stu-id="94715-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="94715-107">示例</span><span class="sxs-lookup"><span data-stu-id="94715-107">EXAMPLES</span></span>

### <span data-ttu-id="94715-108">範例1：儲存配置變更</span><span class="sxs-lookup"><span data-stu-id="94715-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="94715-109">這個命令會透過建立具有目前配置快照的認可來儲存變更至存儲庫中的指定分支。</span><span class="sxs-lookup"><span data-stu-id="94715-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="94715-110">參數</span><span class="sxs-lookup"><span data-stu-id="94715-110">PARAMETERS</span></span>

### <span data-ttu-id="94715-111">-分支</span><span class="sxs-lookup"><span data-stu-id="94715-111">-Branch</span></span>
<span data-ttu-id="94715-112">指定要在其中提交目前配置快照的 Git 分支的名稱。</span><span class="sxs-lookup"><span data-stu-id="94715-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="94715-113">-內容</span><span class="sxs-lookup"><span data-stu-id="94715-113">-Context</span></span>
<span data-ttu-id="94715-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="94715-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="94715-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94715-115">-DefaultProfile</span></span>
<span data-ttu-id="94715-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94715-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="94715-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94715-117">-Force</span></span>
<span data-ttu-id="94715-118">指定此 Cmdlet 會將目前的設定資料庫提交到 Git 儲存庫，即使 Git 儲存庫中有覆蓋的更新變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="94715-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="94715-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94715-119">-PassThru</span></span>
<span data-ttu-id="94715-120">指示這個 Cmdlet 會傳回 **PsApiManagementOperationResult** 物件。</span><span class="sxs-lookup"><span data-stu-id="94715-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="94715-121">-確認</span><span class="sxs-lookup"><span data-stu-id="94715-121">-Confirm</span></span>
<span data-ttu-id="94715-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94715-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94715-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94715-123">-WhatIf</span></span>
<span data-ttu-id="94715-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94715-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94715-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94715-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94715-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94715-126">CommonParameters</span></span>
<span data-ttu-id="94715-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94715-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94715-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94715-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94715-129">輸入</span><span class="sxs-lookup"><span data-stu-id="94715-129">INPUTS</span></span>

### <span data-ttu-id="94715-130">所有</span><span class="sxs-lookup"><span data-stu-id="94715-130">None</span></span>
<span data-ttu-id="94715-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="94715-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94715-132">輸出</span><span class="sxs-lookup"><span data-stu-id="94715-132">OUTPUTS</span></span>

### <span data-ttu-id="94715-133">ServiceManagement. PsApiManagementOperationResult （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="94715-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="94715-134">筆記</span><span class="sxs-lookup"><span data-stu-id="94715-134">NOTES</span></span>

## <span data-ttu-id="94715-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="94715-135">RELATED LINKS</span></span>

[<span data-ttu-id="94715-136">發佈-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="94715-136">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


