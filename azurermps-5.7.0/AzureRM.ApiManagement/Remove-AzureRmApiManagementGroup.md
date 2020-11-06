---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454783"
---
# <span data-ttu-id="43f93-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="43f93-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="43f93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43f93-102">SYNOPSIS</span></span>
<span data-ttu-id="43f93-103">移除現有的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="43f93-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f93-104">句法</span><span class="sxs-lookup"><span data-stu-id="43f93-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f93-105">說明</span><span class="sxs-lookup"><span data-stu-id="43f93-105">DESCRIPTION</span></span>
<span data-ttu-id="43f93-106">AzureRmApiManagementGroup Cmdlet 會移除現有 **的** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="43f93-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="43f93-107">示例</span><span class="sxs-lookup"><span data-stu-id="43f93-107">EXAMPLES</span></span>

### <span data-ttu-id="43f93-108">範例1：移除現有的管理群組</span><span class="sxs-lookup"><span data-stu-id="43f93-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="43f93-109">這個命令會移除名為 Group0001 的現有管理組，不會提示使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="43f93-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="43f93-110">參數</span><span class="sxs-lookup"><span data-stu-id="43f93-110">PARAMETERS</span></span>

### <span data-ttu-id="43f93-111">-內容</span><span class="sxs-lookup"><span data-stu-id="43f93-111">-Context</span></span>
<span data-ttu-id="43f93-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="43f93-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="43f93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f93-113">-DefaultProfile</span></span>
<span data-ttu-id="43f93-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43f93-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="43f93-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="43f93-115">-GroupId</span></span>
<span data-ttu-id="43f93-116">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43f93-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="43f93-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43f93-117">-PassThru</span></span>
<span data-ttu-id="43f93-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="43f93-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="43f93-119">-確認</span><span class="sxs-lookup"><span data-stu-id="43f93-119">-Confirm</span></span>
<span data-ttu-id="43f93-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43f93-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f93-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f93-121">-WhatIf</span></span>
<span data-ttu-id="43f93-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43f93-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f93-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43f93-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f93-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f93-124">CommonParameters</span></span>
<span data-ttu-id="43f93-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43f93-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f93-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43f93-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f93-127">輸入</span><span class="sxs-lookup"><span data-stu-id="43f93-127">INPUTS</span></span>

### <span data-ttu-id="43f93-128">所有</span><span class="sxs-lookup"><span data-stu-id="43f93-128">None</span></span>
<span data-ttu-id="43f93-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="43f93-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43f93-130">輸出</span><span class="sxs-lookup"><span data-stu-id="43f93-130">OUTPUTS</span></span>

### <span data-ttu-id="43f93-131">布林值</span><span class="sxs-lookup"><span data-stu-id="43f93-131">Boolean</span></span>

## <span data-ttu-id="43f93-132">筆記</span><span class="sxs-lookup"><span data-stu-id="43f93-132">NOTES</span></span>

## <span data-ttu-id="43f93-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="43f93-133">RELATED LINKS</span></span>

[<span data-ttu-id="43f93-134">AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="43f93-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="43f93-135">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="43f93-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="43f93-136">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="43f93-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


