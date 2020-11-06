---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 561bec75ecfe59c65b2b8ea6ac71364573aa2bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613931"
---
# <span data-ttu-id="3aa90-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3aa90-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="3aa90-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3aa90-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa90-103">移除現有的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="3aa90-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="3aa90-104">句法</span><span class="sxs-lookup"><span data-stu-id="3aa90-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aa90-105">說明</span><span class="sxs-lookup"><span data-stu-id="3aa90-105">DESCRIPTION</span></span>
<span data-ttu-id="3aa90-106">AzApiManagementGroup Cmdlet 會移除現有 **的** API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="3aa90-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="3aa90-107">示例</span><span class="sxs-lookup"><span data-stu-id="3aa90-107">EXAMPLES</span></span>

### <span data-ttu-id="3aa90-108">範例1：移除現有的管理群組</span><span class="sxs-lookup"><span data-stu-id="3aa90-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="3aa90-109">這個命令會移除名為 Group0001 的現有管理組，不會提示使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="3aa90-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="3aa90-110">參數</span><span class="sxs-lookup"><span data-stu-id="3aa90-110">PARAMETERS</span></span>

### <span data-ttu-id="3aa90-111">-內容</span><span class="sxs-lookup"><span data-stu-id="3aa90-111">-Context</span></span>
<span data-ttu-id="3aa90-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="3aa90-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3aa90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa90-113">-DefaultProfile</span></span>
<span data-ttu-id="3aa90-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3aa90-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aa90-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3aa90-115">-GroupId</span></span>
<span data-ttu-id="3aa90-116">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3aa90-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="3aa90-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3aa90-117">-PassThru</span></span>
<span data-ttu-id="3aa90-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="3aa90-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="3aa90-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3aa90-119">-Confirm</span></span>
<span data-ttu-id="3aa90-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3aa90-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa90-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa90-121">-WhatIf</span></span>
<span data-ttu-id="3aa90-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3aa90-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aa90-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3aa90-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa90-124">CommonParameters</span></span>
<span data-ttu-id="3aa90-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3aa90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa90-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3aa90-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa90-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3aa90-127">INPUTS</span></span>

### <span data-ttu-id="3aa90-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3aa90-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3aa90-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3aa90-129">System.String</span></span>

### <span data-ttu-id="3aa90-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="3aa90-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3aa90-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3aa90-131">OUTPUTS</span></span>

### <span data-ttu-id="3aa90-132">System.object</span><span class="sxs-lookup"><span data-stu-id="3aa90-132">System.Boolean</span></span>

## <span data-ttu-id="3aa90-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3aa90-133">NOTES</span></span>

## <span data-ttu-id="3aa90-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3aa90-134">RELATED LINKS</span></span>

[<span data-ttu-id="3aa90-135">AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3aa90-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="3aa90-136">新-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3aa90-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="3aa90-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3aa90-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


