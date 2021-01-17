---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449487"
---
# <span data-ttu-id="c9792-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="c9792-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="c9792-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9792-102">SYNOPSIS</span></span>
<span data-ttu-id="c9792-103">取得特定作業的 databox 認證</span><span class="sxs-lookup"><span data-stu-id="c9792-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="c9792-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9792-104">SYNTAX</span></span>

### <span data-ttu-id="c9792-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c9792-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9792-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9792-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9792-107">說明</span><span class="sxs-lookup"><span data-stu-id="c9792-107">DESCRIPTION</span></span>
<span data-ttu-id="c9792-108">**AzDataBoxCredential** Cmdlet 會取得特定作業之 databox 的認證。</span><span class="sxs-lookup"><span data-stu-id="c9792-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="c9792-109">針對不同的 Sku 類型，傳回的認證物件的內部屬性會有所不同。</span><span class="sxs-lookup"><span data-stu-id="c9792-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="c9792-110">示例</span><span class="sxs-lookup"><span data-stu-id="c9792-110">EXAMPLES</span></span>

### <span data-ttu-id="c9792-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c9792-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="c9792-112">這會 retuns 指定作業的 JobSecrets</span><span class="sxs-lookup"><span data-stu-id="c9792-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="c9792-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c9792-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="c9792-114">這會 retuns 指定作業的 JobSecrets</span><span class="sxs-lookup"><span data-stu-id="c9792-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="c9792-115">參數</span><span class="sxs-lookup"><span data-stu-id="c9792-115">PARAMETERS</span></span>

### <span data-ttu-id="c9792-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9792-116">-DefaultProfile</span></span>
<span data-ttu-id="c9792-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9792-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9792-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9792-118">-Name</span></span>
<span data-ttu-id="c9792-119">Databox 工作名稱</span><span class="sxs-lookup"><span data-stu-id="c9792-119">Databox Job Name</span></span>

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

### <span data-ttu-id="c9792-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9792-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9792-121">Databox 工作資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c9792-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="c9792-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9792-122">-ResourceId</span></span>
<span data-ttu-id="c9792-123">Databox 工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c9792-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="c9792-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9792-124">CommonParameters</span></span>
<span data-ttu-id="c9792-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9792-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9792-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9792-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9792-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c9792-127">INPUTS</span></span>

### <span data-ttu-id="c9792-128">System.object</span><span class="sxs-lookup"><span data-stu-id="c9792-128">System.String</span></span>

## <span data-ttu-id="c9792-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c9792-129">OUTPUTS</span></span>

### <span data-ttu-id="c9792-130">System.object. IEnumerable ' 1 [DataBox. UnencryptedCredentials，DataBox，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = 31bf3856ad364e35]]）。））））</span><span class="sxs-lookup"><span data-stu-id="c9792-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c9792-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c9792-131">NOTES</span></span>

## <span data-ttu-id="c9792-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9792-132">RELATED LINKS</span></span>
