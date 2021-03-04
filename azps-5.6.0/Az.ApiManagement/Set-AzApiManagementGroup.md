---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: c243cd47300d2b361e37766ab7e2e5bc906cb2ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905277"
---
# <span data-ttu-id="1c04e-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c04e-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="1c04e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c04e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c04e-103">設定 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="1c04e-103">Configures an API management group.</span></span>

## <span data-ttu-id="1c04e-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c04e-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c04e-105">描述</span><span class="sxs-lookup"><span data-stu-id="1c04e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c04e-106">**Set-AzApiManagementGroup** Cmdlet 會設定 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="1c04e-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="1c04e-107">例子</span><span class="sxs-lookup"><span data-stu-id="1c04e-107">EXAMPLES</span></span>

### <span data-ttu-id="1c04e-108">範例 1：設定管理群組</span><span class="sxs-lookup"><span data-stu-id="1c04e-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="1c04e-109">此命令會設定名為 Group0001 的管理群組。</span><span class="sxs-lookup"><span data-stu-id="1c04e-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="1c04e-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c04e-110">PARAMETERS</span></span>

### <span data-ttu-id="1c04e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="1c04e-111">-Context</span></span>
<span data-ttu-id="1c04e-112">指定 **PsApiManagementCoNtext 物件的** 實例。</span><span class="sxs-lookup"><span data-stu-id="1c04e-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1c04e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c04e-113">-DefaultProfile</span></span>
<span data-ttu-id="1c04e-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c04e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c04e-115">-描述</span><span class="sxs-lookup"><span data-stu-id="1c04e-115">-Description</span></span>
<span data-ttu-id="1c04e-116">指定管理群組的描述。</span><span class="sxs-lookup"><span data-stu-id="1c04e-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c04e-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1c04e-117">-GroupId</span></span>
<span data-ttu-id="1c04e-118">指定管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c04e-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="1c04e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c04e-119">-Name</span></span>
<span data-ttu-id="1c04e-120">指定管理組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c04e-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c04e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c04e-121">-PassThru</span></span>
<span data-ttu-id="1c04e-122">Passthru</span><span class="sxs-lookup"><span data-stu-id="1c04e-122">passthru</span></span>

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

### <span data-ttu-id="1c04e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1c04e-123">-Confirm</span></span>
<span data-ttu-id="1c04e-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1c04e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c04e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c04e-125">-WhatIf</span></span>
<span data-ttu-id="1c04e-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c04e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c04e-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c04e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c04e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c04e-128">CommonParameters</span></span>
<span data-ttu-id="1c04e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c04e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c04e-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c04e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c04e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1c04e-131">INPUTS</span></span>

### <span data-ttu-id="1c04e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="1c04e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c04e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1c04e-133">System.String</span></span>

### <span data-ttu-id="1c04e-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c04e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c04e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1c04e-135">OUTPUTS</span></span>

### <span data-ttu-id="1c04e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c04e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="1c04e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1c04e-137">NOTES</span></span>

## <span data-ttu-id="1c04e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c04e-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c04e-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c04e-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="1c04e-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c04e-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="1c04e-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c04e-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


