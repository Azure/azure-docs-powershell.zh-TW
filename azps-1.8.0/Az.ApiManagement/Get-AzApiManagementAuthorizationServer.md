---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 2624ccad63b2992ef8cae889cea04b849658444e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611632"
---
# <span data-ttu-id="91aed-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91aed-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="91aed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91aed-102">SYNOPSIS</span></span>
<span data-ttu-id="91aed-103">取得 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="91aed-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="91aed-104">句法</span><span class="sxs-lookup"><span data-stu-id="91aed-104">SYNTAX</span></span>

### <span data-ttu-id="91aed-105">GetAllAuthorizationServers (預設) </span><span class="sxs-lookup"><span data-stu-id="91aed-105">GetAllAuthorizationServers (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91aed-106">GetByServerId</span><span class="sxs-lookup"><span data-stu-id="91aed-106">GetByServerId</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91aed-107">說明</span><span class="sxs-lookup"><span data-stu-id="91aed-107">DESCRIPTION</span></span>
<span data-ttu-id="91aed-108">**AzApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="91aed-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="91aed-109">示例</span><span class="sxs-lookup"><span data-stu-id="91aed-109">EXAMPLES</span></span>

### <span data-ttu-id="91aed-110">範例1：取得所有授權伺服器</span><span class="sxs-lookup"><span data-stu-id="91aed-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="91aed-111">這個命令會取得所有 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="91aed-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="91aed-112">範例2：取得指定的授權伺服器</span><span class="sxs-lookup"><span data-stu-id="91aed-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="91aed-113">這個命令會取得指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="91aed-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="91aed-114">參數</span><span class="sxs-lookup"><span data-stu-id="91aed-114">PARAMETERS</span></span>

### <span data-ttu-id="91aed-115">-內容</span><span class="sxs-lookup"><span data-stu-id="91aed-115">-Context</span></span>

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

### <span data-ttu-id="91aed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91aed-116">-DefaultProfile</span></span>
<span data-ttu-id="91aed-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91aed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91aed-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="91aed-118">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: GetByServerId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91aed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91aed-119">CommonParameters</span></span>
<span data-ttu-id="91aed-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91aed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91aed-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91aed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91aed-122">輸入</span><span class="sxs-lookup"><span data-stu-id="91aed-122">INPUTS</span></span>

### <span data-ttu-id="91aed-123">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="91aed-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91aed-124">System.object</span><span class="sxs-lookup"><span data-stu-id="91aed-124">System.String</span></span>

## <span data-ttu-id="91aed-125">輸出</span><span class="sxs-lookup"><span data-stu-id="91aed-125">OUTPUTS</span></span>

### <span data-ttu-id="91aed-126">ServiceManagement. PsApiManagementOAuth2AuthrozationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="91aed-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="91aed-127">筆記</span><span class="sxs-lookup"><span data-stu-id="91aed-127">NOTES</span></span>

## <span data-ttu-id="91aed-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="91aed-128">RELATED LINKS</span></span>

[<span data-ttu-id="91aed-129">新-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91aed-129">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="91aed-130">移除-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91aed-130">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="91aed-131">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="91aed-131">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


