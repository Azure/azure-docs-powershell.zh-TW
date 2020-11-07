---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: df342b3ec96f8bfa8ba882bac2ae620456286012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788881"
---
# <span data-ttu-id="068bf-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="068bf-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="068bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="068bf-102">SYNOPSIS</span></span>
<span data-ttu-id="068bf-103">移除 API。</span><span class="sxs-lookup"><span data-stu-id="068bf-103">Removes an API.</span></span>

## <span data-ttu-id="068bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="068bf-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="068bf-105">DESCRIPTION</span></span>
<span data-ttu-id="068bf-106">AzApiManagementApi Cmdlet 會移除現有 **的** API。</span><span class="sxs-lookup"><span data-stu-id="068bf-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="068bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="068bf-107">EXAMPLES</span></span>

### <span data-ttu-id="068bf-108">範例1：移除 API</span><span class="sxs-lookup"><span data-stu-id="068bf-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="068bf-109">這個命令會移除具有指定識別碼的 API。</span><span class="sxs-lookup"><span data-stu-id="068bf-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="068bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="068bf-110">PARAMETERS</span></span>

### <span data-ttu-id="068bf-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="068bf-111">-ApiId</span></span>
<span data-ttu-id="068bf-112">指定 API 移除的識別碼。</span><span class="sxs-lookup"><span data-stu-id="068bf-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="068bf-113">-內容</span><span class="sxs-lookup"><span data-stu-id="068bf-113">-Context</span></span>
<span data-ttu-id="068bf-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="068bf-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="068bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068bf-115">-DefaultProfile</span></span>
<span data-ttu-id="068bf-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="068bf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="068bf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="068bf-117">-PassThru</span></span>
<span data-ttu-id="068bf-118">passthru</span><span class="sxs-lookup"><span data-stu-id="068bf-118">passthru</span></span>

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

### <span data-ttu-id="068bf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="068bf-119">-Confirm</span></span>
<span data-ttu-id="068bf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="068bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="068bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068bf-121">-WhatIf</span></span>
<span data-ttu-id="068bf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="068bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="068bf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="068bf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="068bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068bf-124">CommonParameters</span></span>
<span data-ttu-id="068bf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="068bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068bf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="068bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068bf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="068bf-127">INPUTS</span></span>

### <span data-ttu-id="068bf-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="068bf-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="068bf-129">System.object</span><span class="sxs-lookup"><span data-stu-id="068bf-129">System.String</span></span>

### <span data-ttu-id="068bf-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="068bf-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="068bf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="068bf-131">OUTPUTS</span></span>

### <span data-ttu-id="068bf-132">System.object</span><span class="sxs-lookup"><span data-stu-id="068bf-132">System.Boolean</span></span>

## <span data-ttu-id="068bf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="068bf-133">NOTES</span></span>

## <span data-ttu-id="068bf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="068bf-134">RELATED LINKS</span></span>

[<span data-ttu-id="068bf-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="068bf-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="068bf-136">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="068bf-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="068bf-137">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="068bf-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="068bf-138">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="068bf-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="068bf-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="068bf-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


