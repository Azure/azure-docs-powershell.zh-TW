---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135395"
---
# <span data-ttu-id="73729-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="73729-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="73729-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73729-102">SYNOPSIS</span></span>
<span data-ttu-id="73729-103">在租使用者範圍中取得部署的部署作業</span><span class="sxs-lookup"><span data-stu-id="73729-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="73729-104">句法</span><span class="sxs-lookup"><span data-stu-id="73729-104">SYNTAX</span></span>

### <span data-ttu-id="73729-105">GetByDeploymentName (預設) </span><span class="sxs-lookup"><span data-stu-id="73729-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73729-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="73729-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73729-107">說明</span><span class="sxs-lookup"><span data-stu-id="73729-107">DESCRIPTION</span></span>
<span data-ttu-id="73729-108">**AzTenantDeploymentOperation** Cmdlet 會列出屬於目前租使用者範圍內部署的所有作業，以協助您識別並提供有關特定部署失敗之確切作業的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="73729-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="73729-109">示例</span><span class="sxs-lookup"><span data-stu-id="73729-109">EXAMPLES</span></span>

### <span data-ttu-id="73729-110">範例1：取得給定部署名稱的部署作業</span><span class="sxs-lookup"><span data-stu-id="73729-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="73729-111">取得目前租使用者範圍中名稱為 "Deploy01" 的部署作業。</span><span class="sxs-lookup"><span data-stu-id="73729-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="73729-112">範例2：取得部署並取得其部署作業</span><span class="sxs-lookup"><span data-stu-id="73729-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="73729-113">這個命令會在目前的租使用者範圍中取得部署 "Deploy01"，並取得其部署作業。</span><span class="sxs-lookup"><span data-stu-id="73729-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="73729-114">參數</span><span class="sxs-lookup"><span data-stu-id="73729-114">PARAMETERS</span></span>

### <span data-ttu-id="73729-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73729-115">-DefaultProfile</span></span>
<span data-ttu-id="73729-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73729-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73729-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="73729-117">-DeploymentName</span></span>
<span data-ttu-id="73729-118">部署名稱。</span><span class="sxs-lookup"><span data-stu-id="73729-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73729-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="73729-119">-DeploymentObject</span></span>
<span data-ttu-id="73729-120">部署物件。</span><span class="sxs-lookup"><span data-stu-id="73729-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73729-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="73729-121">-OperationId</span></span>
<span data-ttu-id="73729-122">部署操作 Id。</span><span class="sxs-lookup"><span data-stu-id="73729-122">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73729-123">-預先</span><span class="sxs-lookup"><span data-stu-id="73729-123">-Pre</span></span>
<span data-ttu-id="73729-124">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="73729-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="73729-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73729-125">CommonParameters</span></span>
<span data-ttu-id="73729-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73729-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73729-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73729-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73729-128">輸入</span><span class="sxs-lookup"><span data-stu-id="73729-128">INPUTS</span></span>

### <span data-ttu-id="73729-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="73729-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="73729-130">輸出</span><span class="sxs-lookup"><span data-stu-id="73729-130">OUTPUTS</span></span>

### <span data-ttu-id="73729-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="73729-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="73729-132">筆記</span><span class="sxs-lookup"><span data-stu-id="73729-132">NOTES</span></span>

## <span data-ttu-id="73729-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="73729-133">RELATED LINKS</span></span>
