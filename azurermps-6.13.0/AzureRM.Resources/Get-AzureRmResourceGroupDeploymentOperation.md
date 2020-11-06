---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 145c71001fa0812681ab3975fccbb0167de5d978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448258"
---
# <span data-ttu-id="2bfb5-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2bfb5-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="2bfb5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bfb5-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfb5-103">取得資源群組部署作業</span><span class="sxs-lookup"><span data-stu-id="2bfb5-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bfb5-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bfb5-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2bfb5-105">說明</span><span class="sxs-lookup"><span data-stu-id="2bfb5-105">DESCRIPTION</span></span>
<span data-ttu-id="2bfb5-106">**AzureRmResourceGroupDeploymentOperation** Cmdlet 會列出部署中的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="2bfb5-107">它也可以顯示每個部署作業的回應和要求內容。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="2bfb5-108">這與入口網站上的部署詳細資料中提供的資訊相同。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="2bfb5-109">若要取得要求和回應內容，請在透過 **新的 AzureRmResourceGroupDeployment** 提交部署時啟用此設定。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="2bfb5-110">它可能會記錄和公開在您檢索部署作業時傳回的資源屬性或 **listKeys** 作業中所使用的密碼等機密。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="2bfb5-111">如需此設定及如何啟用的詳細資訊，請參閱 New-AzureRmResourceGroupDeployment 與調試 ARM 範本部署</span><span class="sxs-lookup"><span data-stu-id="2bfb5-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="2bfb5-112">示例</span><span class="sxs-lookup"><span data-stu-id="2bfb5-112">EXAMPLES</span></span>

### <span data-ttu-id="2bfb5-113">Get1</span><span class="sxs-lookup"><span data-stu-id="2bfb5-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="2bfb5-114">取得資源群組「test」下名稱為「test」的部署作業</span><span class="sxs-lookup"><span data-stu-id="2bfb5-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="2bfb5-115">參數</span><span class="sxs-lookup"><span data-stu-id="2bfb5-115">PARAMETERS</span></span>

### <span data-ttu-id="2bfb5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2bfb5-116">-ApiVersion</span></span>
<span data-ttu-id="2bfb5-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2bfb5-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2bfb5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bfb5-119">-DefaultProfile</span></span>
<span data-ttu-id="2bfb5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2bfb5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bfb5-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="2bfb5-121">-DeploymentName</span></span>
<span data-ttu-id="2bfb5-122">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-122">The deployment name.</span></span>

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

### <span data-ttu-id="2bfb5-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2bfb5-123">-InformationAction</span></span>
<span data-ttu-id="2bfb5-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2bfb5-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2bfb5-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2bfb5-126">持續</span><span class="sxs-lookup"><span data-stu-id="2bfb5-126">Continue</span></span>
- <span data-ttu-id="2bfb5-127">理會</span><span class="sxs-lookup"><span data-stu-id="2bfb5-127">Ignore</span></span>
- <span data-ttu-id="2bfb5-128">看</span><span class="sxs-lookup"><span data-stu-id="2bfb5-128">Inquire</span></span>
- <span data-ttu-id="2bfb5-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2bfb5-129">SilentlyContinue</span></span>
- <span data-ttu-id="2bfb5-130">停止</span><span class="sxs-lookup"><span data-stu-id="2bfb5-130">Stop</span></span>
- <span data-ttu-id="2bfb5-131">封存</span><span class="sxs-lookup"><span data-stu-id="2bfb5-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfb5-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2bfb5-132">-InformationVariable</span></span>
<span data-ttu-id="2bfb5-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bfb5-134">-預先</span><span class="sxs-lookup"><span data-stu-id="2bfb5-134">-Pre</span></span>
<span data-ttu-id="2bfb5-135">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2bfb5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfb5-136">-ResourceGroupName</span></span>
<span data-ttu-id="2bfb5-137">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-137">The resource group name.</span></span>

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

### <span data-ttu-id="2bfb5-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bfb5-138">-SubscriptionId</span></span>
<span data-ttu-id="2bfb5-139">要使用的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-139">The subscription to use.</span></span>

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

### <span data-ttu-id="2bfb5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfb5-140">CommonParameters</span></span>
<span data-ttu-id="2bfb5-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfb5-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bfb5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfb5-143">輸入</span><span class="sxs-lookup"><span data-stu-id="2bfb5-143">INPUTS</span></span>

## <span data-ttu-id="2bfb5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2bfb5-144">OUTPUTS</span></span>

## <span data-ttu-id="2bfb5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2bfb5-145">NOTES</span></span>

## <span data-ttu-id="2bfb5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bfb5-146">RELATED LINKS</span></span>
