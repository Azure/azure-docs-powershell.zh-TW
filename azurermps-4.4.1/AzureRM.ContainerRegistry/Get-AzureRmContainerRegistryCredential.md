---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450816"
---
# <span data-ttu-id="9add7-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9add7-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="9add7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9add7-102">SYNOPSIS</span></span>
<span data-ttu-id="9add7-103">取得容器註冊的登入認證。</span><span class="sxs-lookup"><span data-stu-id="9add7-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9add7-104">句法</span><span class="sxs-lookup"><span data-stu-id="9add7-104">SYNTAX</span></span>

### <span data-ttu-id="9add7-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9add7-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9add7-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9add7-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9add7-107">說明</span><span class="sxs-lookup"><span data-stu-id="9add7-107">DESCRIPTION</span></span>
<span data-ttu-id="9add7-108">AzureRmContainerRegistryCredential Cmdlet 會取得容器註冊的登 **入** 認證。</span><span class="sxs-lookup"><span data-stu-id="9add7-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="9add7-109">示例</span><span class="sxs-lookup"><span data-stu-id="9add7-109">EXAMPLES</span></span>

### <span data-ttu-id="9add7-110">範例1：取得容器註冊的登入認證</span><span class="sxs-lookup"><span data-stu-id="9add7-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="9add7-111">這個命令會取得指定之容器註冊表的登入認證。</span><span class="sxs-lookup"><span data-stu-id="9add7-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="9add7-112">管理員使用者必須啟用容器 `MyRegistry` 登錄，才能取得登入認證。</span><span class="sxs-lookup"><span data-stu-id="9add7-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="9add7-113">參數</span><span class="sxs-lookup"><span data-stu-id="9add7-113">PARAMETERS</span></span>

### <span data-ttu-id="9add7-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="9add7-114">-Name</span></span>
<span data-ttu-id="9add7-115">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="9add7-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9add7-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="9add7-116">-Registry</span></span>
<span data-ttu-id="9add7-117">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="9add7-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9add7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9add7-118">-ResourceGroupName</span></span>
<span data-ttu-id="9add7-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9add7-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9add7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9add7-120">-DefaultProfile</span></span>
<span data-ttu-id="9add7-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9add7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9add7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9add7-122">CommonParameters</span></span>
<span data-ttu-id="9add7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9add7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9add7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9add7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9add7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9add7-125">INPUTS</span></span>

### <span data-ttu-id="9add7-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9add7-126">PSContainerRegistry</span></span>
<span data-ttu-id="9add7-127">參數 "Registry" 接受管線中 "PSContainerRegistry" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9add7-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="9add7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9add7-128">OUTPUTS</span></span>

### <span data-ttu-id="9add7-129">PSContainerRegistryCredential 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9add7-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="9add7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9add7-130">NOTES</span></span>

## <span data-ttu-id="9add7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9add7-131">RELATED LINKS</span></span>

[<span data-ttu-id="9add7-132">新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9add7-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="9add7-133">更新-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9add7-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="9add7-134">更新-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="9add7-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)

