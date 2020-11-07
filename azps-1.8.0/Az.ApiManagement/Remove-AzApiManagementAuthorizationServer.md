---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: cc990e074274917e13b3659aaf0c88f2185f4bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788865"
---
# <span data-ttu-id="f4e40-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f4e40-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="f4e40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4e40-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e40-103">移除授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e40-103">Removes an authorization server.</span></span>

## <span data-ttu-id="f4e40-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4e40-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e40-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4e40-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e40-106">**AzApiManagementAuthorizationServer** Cmdlet 會移除 Azure API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e40-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="f4e40-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4e40-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e40-108">範例1：移除授權伺服器</span><span class="sxs-lookup"><span data-stu-id="f4e40-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="f4e40-109">這個命令會移除指定的 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e40-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="f4e40-110">由於已指定 *Force* 參數，因此不需要確認。</span><span class="sxs-lookup"><span data-stu-id="f4e40-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="f4e40-111">參數</span><span class="sxs-lookup"><span data-stu-id="f4e40-111">PARAMETERS</span></span>

### <span data-ttu-id="f4e40-112">-內容</span><span class="sxs-lookup"><span data-stu-id="f4e40-112">-Context</span></span>
<span data-ttu-id="f4e40-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f4e40-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4e40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e40-114">-DefaultProfile</span></span>
<span data-ttu-id="f4e40-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4e40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e40-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4e40-116">-PassThru</span></span>
<span data-ttu-id="f4e40-117">passthru</span><span class="sxs-lookup"><span data-stu-id="f4e40-117">passthru</span></span>

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

### <span data-ttu-id="f4e40-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="f4e40-118">-ServerId</span></span>
<span data-ttu-id="f4e40-119">指定要移除的授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4e40-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="f4e40-120">-確認</span><span class="sxs-lookup"><span data-stu-id="f4e40-120">-Confirm</span></span>
<span data-ttu-id="f4e40-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4e40-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e40-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e40-122">-WhatIf</span></span>
<span data-ttu-id="f4e40-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4e40-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4e40-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4e40-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e40-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e40-125">CommonParameters</span></span>
<span data-ttu-id="f4e40-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4e40-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e40-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4e40-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e40-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f4e40-128">INPUTS</span></span>

### <span data-ttu-id="f4e40-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f4e40-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4e40-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f4e40-130">System.String</span></span>

### <span data-ttu-id="f4e40-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f4e40-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4e40-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f4e40-132">OUTPUTS</span></span>

### <span data-ttu-id="f4e40-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f4e40-133">System.Boolean</span></span>

## <span data-ttu-id="f4e40-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f4e40-134">NOTES</span></span>

## <span data-ttu-id="f4e40-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4e40-135">RELATED LINKS</span></span>

[<span data-ttu-id="f4e40-136">AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f4e40-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="f4e40-137">新-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f4e40-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="f4e40-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f4e40-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


