---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445232"
---
# <span data-ttu-id="adea0-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="adea0-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="adea0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adea0-102">SYNOPSIS</span></span>
<span data-ttu-id="adea0-103">取得清單或特定的 API 管理服務描述。</span><span class="sxs-lookup"><span data-stu-id="adea0-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adea0-104">句法</span><span class="sxs-lookup"><span data-stu-id="adea0-104">SYNTAX</span></span>

### <span data-ttu-id="adea0-105">[全部在訂閱] 中 (預設) </span><span class="sxs-lookup"><span data-stu-id="adea0-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adea0-106">[資源群組] 中的 [全部]</span><span class="sxs-lookup"><span data-stu-id="adea0-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="adea0-107">特定 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="adea0-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adea0-108">說明</span><span class="sxs-lookup"><span data-stu-id="adea0-108">DESCRIPTION</span></span>
<span data-ttu-id="adea0-109">**AzureRmApiManagement** Cmdlet 會取得 [訂閱] 或 [指定的資源] 群組或特定 API 管理下的所有 API 管理服務清單。</span><span class="sxs-lookup"><span data-stu-id="adea0-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="adea0-110">示例</span><span class="sxs-lookup"><span data-stu-id="adea0-110">EXAMPLES</span></span>

### <span data-ttu-id="adea0-111">範例1：取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="adea0-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="adea0-112">這個命令會取得訂閱中的所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="adea0-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="adea0-113">範例2：以特定名稱取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="adea0-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="adea0-114">這個命令會透過名稱取得所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="adea0-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="adea0-115">參數</span><span class="sxs-lookup"><span data-stu-id="adea0-115">PARAMETERS</span></span>

### <span data-ttu-id="adea0-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="adea0-116">-Name</span></span>
<span data-ttu-id="adea0-117">指定 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="adea0-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adea0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adea0-118">-ResourceGroupName</span></span>
<span data-ttu-id="adea0-119">指定此 Cmdlet 取得 API 管理服務所依據之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="adea0-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adea0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adea0-120">-DefaultProfile</span></span>
<span data-ttu-id="adea0-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="adea0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adea0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adea0-122">CommonParameters</span></span>
<span data-ttu-id="adea0-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adea0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adea0-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="adea0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adea0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="adea0-125">INPUTS</span></span>

## <span data-ttu-id="adea0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="adea0-126">OUTPUTS</span></span>

### <span data-ttu-id="adea0-127">[System.object]. 清單 ' 1 [ApiManagement]。 PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="adea0-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="adea0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="adea0-128">NOTES</span></span>

## <span data-ttu-id="adea0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="adea0-129">RELATED LINKS</span></span>

[<span data-ttu-id="adea0-130">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="adea0-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="adea0-131">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="adea0-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="adea0-132">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="adea0-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="adea0-133">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="adea0-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


