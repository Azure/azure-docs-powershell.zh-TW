---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: fd0e6c1def47871966821adf0c6a29f4345d5851
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959856"
---
# <span data-ttu-id="8f26d-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8f26d-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="8f26d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f26d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f26d-103">取得資源群組部署作業</span><span class="sxs-lookup"><span data-stu-id="8f26d-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="8f26d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f26d-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f26d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f26d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f26d-106">**AzResourceGroupDeploymentOperation** Cmdlet 會列出部署中的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8f26d-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="8f26d-107">它也可以顯示每個部署作業的回應和要求內容。</span><span class="sxs-lookup"><span data-stu-id="8f26d-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="8f26d-108">這與入口網站上的部署詳細資料中提供的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="8f26d-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="8f26d-109">若要取得要求和回應內容，請在透過 **新的 AzResourceGroupDeployment** 提交部署時啟用此設定。</span><span class="sxs-lookup"><span data-stu-id="8f26d-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="8f26d-110">它可能會記錄和公開在您檢索部署作業時傳回的資源屬性或 **listKeys** 作業中所使用的密碼等機密。</span><span class="sxs-lookup"><span data-stu-id="8f26d-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="8f26d-111">如需此設定及如何啟用的詳細資訊，請參閱 New-AzResourceGroupDeployment 與調試 ARM 範本部署</span><span class="sxs-lookup"><span data-stu-id="8f26d-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="8f26d-112">示例</span><span class="sxs-lookup"><span data-stu-id="8f26d-112">EXAMPLES</span></span>

### <span data-ttu-id="8f26d-113">Get1</span><span class="sxs-lookup"><span data-stu-id="8f26d-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="8f26d-114">取得資源群組「test」下名稱為「test」的部署作業</span><span class="sxs-lookup"><span data-stu-id="8f26d-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="8f26d-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f26d-115">PARAMETERS</span></span>

### <span data-ttu-id="8f26d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f26d-116">-ApiVersion</span></span>
<span data-ttu-id="8f26d-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8f26d-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f26d-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="8f26d-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f26d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f26d-119">-DefaultProfile</span></span>
<span data-ttu-id="8f26d-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8f26d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f26d-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8f26d-121">-DeploymentName</span></span>
<span data-ttu-id="8f26d-122">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="8f26d-122">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f26d-123">-預先</span><span class="sxs-lookup"><span data-stu-id="8f26d-123">-Pre</span></span>
<span data-ttu-id="8f26d-124">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="8f26d-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8f26d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f26d-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f26d-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f26d-126">The resource group name.</span></span>

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

### <span data-ttu-id="8f26d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f26d-127">-SubscriptionId</span></span>
<span data-ttu-id="8f26d-128">要使用的訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f26d-128">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f26d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f26d-129">CommonParameters</span></span>
<span data-ttu-id="8f26d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f26d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f26d-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8f26d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f26d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8f26d-132">INPUTS</span></span>

### <span data-ttu-id="8f26d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8f26d-133">System.String</span></span>

### <span data-ttu-id="8f26d-134">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f26d-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8f26d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8f26d-135">OUTPUTS</span></span>

### <span data-ttu-id="8f26d-136">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="8f26d-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f26d-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8f26d-137">NOTES</span></span>

## <span data-ttu-id="8f26d-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f26d-138">RELATED LINKS</span></span>
