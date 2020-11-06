---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 99b98bd402d6ac22da4f05ce07a08a2c5980359b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614075"
---
# <span data-ttu-id="6b64e-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b64e-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="6b64e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b64e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b64e-103">取得清單或特定的 API 管理服務描述。</span><span class="sxs-lookup"><span data-stu-id="6b64e-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="6b64e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b64e-104">SYNTAX</span></span>

### <span data-ttu-id="6b64e-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="6b64e-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b64e-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b64e-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b64e-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="6b64e-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b64e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b64e-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b64e-109">說明</span><span class="sxs-lookup"><span data-stu-id="6b64e-109">DESCRIPTION</span></span>
<span data-ttu-id="6b64e-110">**AzApiManagement** Cmdlet 會取得 [訂閱] 或 [指定的資源] 群組或特定 API 管理下的所有 API 管理服務清單。</span><span class="sxs-lookup"><span data-stu-id="6b64e-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="6b64e-111">示例</span><span class="sxs-lookup"><span data-stu-id="6b64e-111">EXAMPLES</span></span>

### <span data-ttu-id="6b64e-112">範例1：取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="6b64e-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="6b64e-113">這個命令會取得訂閱中的所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="6b64e-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="6b64e-114">範例2：以特定名稱取得所有 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="6b64e-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="6b64e-115">這個命令會透過名稱取得所有 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="6b64e-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="6b64e-116">參數</span><span class="sxs-lookup"><span data-stu-id="6b64e-116">PARAMETERS</span></span>

### <span data-ttu-id="6b64e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b64e-117">-DefaultProfile</span></span>
<span data-ttu-id="6b64e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6b64e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b64e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b64e-119">-Name</span></span>
<span data-ttu-id="6b64e-120">指定 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b64e-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b64e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b64e-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b64e-122">指定此 Cmdlet 取得 API 管理服務所依據之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b64e-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b64e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b64e-123">-ResourceId</span></span>
<span data-ttu-id="6b64e-124">API 管理服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="6b64e-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b64e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b64e-125">CommonParameters</span></span>
<span data-ttu-id="6b64e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b64e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b64e-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6b64e-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b64e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6b64e-128">INPUTS</span></span>

### <span data-ttu-id="6b64e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="6b64e-129">System.String</span></span>

## <span data-ttu-id="6b64e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="6b64e-130">OUTPUTS</span></span>

### <span data-ttu-id="6b64e-131">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="6b64e-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="6b64e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6b64e-132">NOTES</span></span>

## <span data-ttu-id="6b64e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b64e-133">RELATED LINKS</span></span>

[<span data-ttu-id="6b64e-134">備份-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b64e-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="6b64e-135">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b64e-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="6b64e-136">移除-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b64e-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="6b64e-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b64e-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


