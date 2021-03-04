---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 4ddeee0b0efbb55d98e8e14be1bc84ea83b38e6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904753"
---
# <span data-ttu-id="cc9af-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cc9af-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="cc9af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc9af-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9af-103">移除現有的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="cc9af-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="cc9af-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc9af-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc9af-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc9af-105">DESCRIPTION</span></span>
<span data-ttu-id="cc9af-106">**Remove-AzApiManagementGroup** Cmdlet 會移除現有的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="cc9af-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="cc9af-107">例子</span><span class="sxs-lookup"><span data-stu-id="cc9af-107">EXAMPLES</span></span>

### <span data-ttu-id="cc9af-108">範例 1：移除現有的管理群組</span><span class="sxs-lookup"><span data-stu-id="cc9af-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="cc9af-109">此命令會移除名為 Group0001 的現有管理群組，不會提示使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cc9af-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="cc9af-110">參數</span><span class="sxs-lookup"><span data-stu-id="cc9af-110">PARAMETERS</span></span>

### <span data-ttu-id="cc9af-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cc9af-111">-Context</span></span>
<span data-ttu-id="cc9af-112">指定 **PsApiManagementCoNtext 物件** 的實例。</span><span class="sxs-lookup"><span data-stu-id="cc9af-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cc9af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9af-113">-DefaultProfile</span></span>
<span data-ttu-id="cc9af-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc9af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc9af-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="cc9af-115">-GroupId</span></span>
<span data-ttu-id="cc9af-116">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc9af-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="cc9af-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc9af-117">-PassThru</span></span>
<span data-ttu-id="cc9af-118">表示此 Cmdlet 如果成功，會$True值，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="cc9af-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="cc9af-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cc9af-119">-Confirm</span></span>
<span data-ttu-id="cc9af-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc9af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc9af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9af-121">-WhatIf</span></span>
<span data-ttu-id="cc9af-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc9af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9af-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc9af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc9af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9af-124">CommonParameters</span></span>
<span data-ttu-id="cc9af-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc9af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9af-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc9af-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9af-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cc9af-127">INPUTS</span></span>

### <span data-ttu-id="cc9af-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="cc9af-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cc9af-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cc9af-129">System.String</span></span>

### <span data-ttu-id="cc9af-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cc9af-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cc9af-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cc9af-131">OUTPUTS</span></span>

### <span data-ttu-id="cc9af-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc9af-132">System.Boolean</span></span>

## <span data-ttu-id="cc9af-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cc9af-133">NOTES</span></span>

## <span data-ttu-id="cc9af-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc9af-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc9af-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cc9af-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="cc9af-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cc9af-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="cc9af-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cc9af-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


