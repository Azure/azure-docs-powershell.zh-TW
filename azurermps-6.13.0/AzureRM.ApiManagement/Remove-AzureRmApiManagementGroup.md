---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: d297c4f8bb9999d60ec694c73aa723dd4afec58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444120"
---
# <span data-ttu-id="d983e-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d983e-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="d983e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d983e-102">SYNOPSIS</span></span>
<span data-ttu-id="d983e-103">移除現有的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="d983e-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d983e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d983e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d983e-105">說明</span><span class="sxs-lookup"><span data-stu-id="d983e-105">DESCRIPTION</span></span>
<span data-ttu-id="d983e-106">AzureRmApiManagementGroup Cmdlet 會移除現有 **的** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="d983e-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="d983e-107">示例</span><span class="sxs-lookup"><span data-stu-id="d983e-107">EXAMPLES</span></span>

### <span data-ttu-id="d983e-108">範例1：移除現有的管理群組</span><span class="sxs-lookup"><span data-stu-id="d983e-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="d983e-109">這個命令會移除名為 Group0001 的現有管理組，不會提示使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="d983e-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="d983e-110">參數</span><span class="sxs-lookup"><span data-stu-id="d983e-110">PARAMETERS</span></span>

### <span data-ttu-id="d983e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="d983e-111">-Context</span></span>
<span data-ttu-id="d983e-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="d983e-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d983e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d983e-113">-DefaultProfile</span></span>
<span data-ttu-id="d983e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d983e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d983e-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d983e-115">-GroupId</span></span>
<span data-ttu-id="d983e-116">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d983e-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="d983e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d983e-117">-PassThru</span></span>
<span data-ttu-id="d983e-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="d983e-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d983e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d983e-119">-Confirm</span></span>
<span data-ttu-id="d983e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d983e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d983e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d983e-121">-WhatIf</span></span>
<span data-ttu-id="d983e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d983e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d983e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d983e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d983e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d983e-124">CommonParameters</span></span>
<span data-ttu-id="d983e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d983e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d983e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d983e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d983e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d983e-127">INPUTS</span></span>

### <span data-ttu-id="d983e-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="d983e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d983e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d983e-129">System.String</span></span>

### <span data-ttu-id="d983e-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d983e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d983e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d983e-131">OUTPUTS</span></span>

### <span data-ttu-id="d983e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="d983e-132">System.Boolean</span></span>

## <span data-ttu-id="d983e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d983e-133">NOTES</span></span>

## <span data-ttu-id="d983e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d983e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d983e-135">AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d983e-135">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d983e-136">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d983e-136">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d983e-137">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d983e-137">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


