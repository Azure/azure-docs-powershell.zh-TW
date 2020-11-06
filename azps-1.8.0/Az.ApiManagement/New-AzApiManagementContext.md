---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623121"
---
# <span data-ttu-id="3fa04-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3fa04-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="3fa04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fa04-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa04-103">建立 PsAzureApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="3fa04-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="3fa04-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fa04-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa04-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fa04-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa04-106">**新的-AzApiManagementCoNtext** Cmdlet 會建立 **PsAzureApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="3fa04-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="3fa04-107">此內容用於所有 API 管理服務 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fa04-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="3fa04-108">示例</span><span class="sxs-lookup"><span data-stu-id="3fa04-108">EXAMPLES</span></span>

### <span data-ttu-id="3fa04-109">範例1：建立 PsApiManagementCoNtext 實例</span><span class="sxs-lookup"><span data-stu-id="3fa04-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="3fa04-110">這個命令會建立 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="3fa04-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="3fa04-111">參數</span><span class="sxs-lookup"><span data-stu-id="3fa04-111">PARAMETERS</span></span>

### <span data-ttu-id="3fa04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa04-112">-DefaultProfile</span></span>
<span data-ttu-id="3fa04-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fa04-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fa04-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa04-114">-ResourceGroupName</span></span>
<span data-ttu-id="3fa04-115">指定部署 API 管理服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fa04-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="3fa04-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3fa04-116">-ServiceName</span></span>
<span data-ttu-id="3fa04-117">指定已部署 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fa04-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="3fa04-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa04-118">CommonParameters</span></span>
<span data-ttu-id="3fa04-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fa04-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa04-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fa04-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa04-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3fa04-121">INPUTS</span></span>

### <span data-ttu-id="3fa04-122">System.object</span><span class="sxs-lookup"><span data-stu-id="3fa04-122">System.String</span></span>

## <span data-ttu-id="3fa04-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3fa04-123">OUTPUTS</span></span>

### <span data-ttu-id="3fa04-124">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3fa04-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3fa04-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3fa04-125">NOTES</span></span>

## <span data-ttu-id="3fa04-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fa04-126">RELATED LINKS</span></span>
