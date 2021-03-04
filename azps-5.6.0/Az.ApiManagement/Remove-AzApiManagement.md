---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: daa4169ed077003d2ceb773e2e085e72fb6d1ec8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903710"
---
# <span data-ttu-id="a8eb7-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8eb7-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="a8eb7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a8eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="a8eb7-103">移除 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-103">Removes an API Management service.</span></span>

## <span data-ttu-id="a8eb7-104">語法</span><span class="sxs-lookup"><span data-stu-id="a8eb7-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8eb7-105">描述</span><span class="sxs-lookup"><span data-stu-id="a8eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="a8eb7-106">**Remove-AzApiManagement** Cmdlet 會移除 Azure API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="a8eb7-107">例子</span><span class="sxs-lookup"><span data-stu-id="a8eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="a8eb7-108">範例 1：移除 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="a8eb7-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="a8eb7-109">此命令會移除名為 ContosoApi 的 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="a8eb7-110">參數</span><span class="sxs-lookup"><span data-stu-id="a8eb7-110">PARAMETERS</span></span>

### <span data-ttu-id="a8eb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8eb7-111">-DefaultProfile</span></span>
<span data-ttu-id="a8eb7-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8eb7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8eb7-113">-Name</span></span>
<span data-ttu-id="a8eb7-114">指定此 Cmdlet 移除的 API 管理部署名稱。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a8eb7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8eb7-115">-PassThru</span></span>
<span data-ttu-id="a8eb7-116">表示如果作業成功，此 Cmdlet 會$True值。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8eb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="a8eb7-118">指定 API 管理部署存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="a8eb7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a8eb7-119">-Confirm</span></span>
<span data-ttu-id="a8eb7-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8eb7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8eb7-121">-WhatIf</span></span>
<span data-ttu-id="a8eb7-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8eb7-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8eb7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8eb7-124">CommonParameters</span></span>
<span data-ttu-id="a8eb7-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a8eb7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8eb7-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8eb7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8eb7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a8eb7-127">INPUTS</span></span>

### <span data-ttu-id="a8eb7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a8eb7-128">System.String</span></span>

## <span data-ttu-id="a8eb7-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a8eb7-129">OUTPUTS</span></span>

### <span data-ttu-id="a8eb7-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8eb7-130">System.Boolean</span></span>

## <span data-ttu-id="a8eb7-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a8eb7-131">NOTES</span></span>

## <span data-ttu-id="a8eb7-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8eb7-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8eb7-133">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8eb7-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="a8eb7-134">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8eb7-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="a8eb7-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8eb7-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="a8eb7-136">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8eb7-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


