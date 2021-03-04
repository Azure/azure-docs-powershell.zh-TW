---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: f5f811b28b349c6dbc9972c9a464a56a002b99f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914109"
---
# <span data-ttu-id="1e14c-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="1e14c-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="1e14c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1e14c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e14c-103">獲得特定工作的資料箱認證</span><span class="sxs-lookup"><span data-stu-id="1e14c-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="1e14c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1e14c-104">SYNTAX</span></span>

### <span data-ttu-id="1e14c-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1e14c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e14c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e14c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e14c-107">描述</span><span class="sxs-lookup"><span data-stu-id="1e14c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e14c-108">**Get-AzDataBoxCredential Cmdlet** 會取得特定工作之資料箱的認證。</span><span class="sxs-lookup"><span data-stu-id="1e14c-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="1e14c-109">針對不同的 SKU 類型，所返回之認證物件的內部屬性會不同。</span><span class="sxs-lookup"><span data-stu-id="1e14c-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="1e14c-110">例子</span><span class="sxs-lookup"><span data-stu-id="1e14c-110">EXAMPLES</span></span>

### <span data-ttu-id="1e14c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="1e14c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="1e14c-112">這會重新調整指定工作的 JobSecrets</span><span class="sxs-lookup"><span data-stu-id="1e14c-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="1e14c-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="1e14c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="1e14c-114">這會重新調整指定工作的 JobSecrets</span><span class="sxs-lookup"><span data-stu-id="1e14c-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="1e14c-115">參數</span><span class="sxs-lookup"><span data-stu-id="1e14c-115">PARAMETERS</span></span>

### <span data-ttu-id="1e14c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e14c-116">-DefaultProfile</span></span>
<span data-ttu-id="1e14c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e14c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e14c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e14c-118">-Name</span></span>
<span data-ttu-id="1e14c-119">資料箱工作名稱</span><span class="sxs-lookup"><span data-stu-id="1e14c-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e14c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e14c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1e14c-121">資料箱工作資源組名</span><span class="sxs-lookup"><span data-stu-id="1e14c-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e14c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e14c-122">-ResourceId</span></span>
<span data-ttu-id="1e14c-123">資料箱工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1e14c-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e14c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e14c-124">CommonParameters</span></span>
<span data-ttu-id="1e14c-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1e14c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e14c-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e14c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e14c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1e14c-127">INPUTS</span></span>

### <span data-ttu-id="1e14c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1e14c-128">System.String</span></span>

## <span data-ttu-id="1e14c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1e14c-129">OUTPUTS</span></span>

### <span data-ttu-id="1e14c-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1e14c-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1e14c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1e14c-131">NOTES</span></span>

## <span data-ttu-id="1e14c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e14c-132">RELATED LINKS</span></span>
