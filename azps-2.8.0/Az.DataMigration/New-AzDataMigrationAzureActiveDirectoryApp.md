---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 2d7a7d61d5a29113f9b0e40340ae6b13b599115f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612724"
---
# <span data-ttu-id="1c623-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="1c623-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="1c623-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c623-102">SYNOPSIS</span></span>
<span data-ttu-id="1c623-103">建立新的實例 DataMigration Azure ActiveDirectory 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1c623-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="1c623-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c623-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c623-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c623-105">DESCRIPTION</span></span>
<span data-ttu-id="1c623-106">建立新的實例 DataMigration Azure ActiveDirectory 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1c623-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="1c623-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c623-107">EXAMPLES</span></span>

### <span data-ttu-id="1c623-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1c623-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="1c623-109">[ApplicationId：「您的 AppId/服務主體識別碼] AppKey： SecureString TenantId： "租使用者識別碼"</span><span class="sxs-lookup"><span data-stu-id="1c623-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="1c623-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c623-110">PARAMETERS</span></span>

### <span data-ttu-id="1c623-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="1c623-111">-AppKey</span></span>
<span data-ttu-id="1c623-112">Azure Active Directory 金鑰</span><span class="sxs-lookup"><span data-stu-id="1c623-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c623-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1c623-113">-ApplicationId</span></span>
<span data-ttu-id="1c623-114">Azure Active Directory 應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="1c623-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c623-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c623-115">-DefaultProfile</span></span>
<span data-ttu-id="1c623-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c623-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c623-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c623-117">CommonParameters</span></span>
<span data-ttu-id="1c623-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c623-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1c623-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c623-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c623-120">輸入</span><span class="sxs-lookup"><span data-stu-id="1c623-120">INPUTS</span></span>

### <span data-ttu-id="1c623-121">所有</span><span class="sxs-lookup"><span data-stu-id="1c623-121">None</span></span>

## <span data-ttu-id="1c623-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1c623-122">OUTPUTS</span></span>

### <span data-ttu-id="1c623-123">PSAzureActiveDirectoryApp 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="1c623-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="1c623-124">筆記</span><span class="sxs-lookup"><span data-stu-id="1c623-124">NOTES</span></span>

## <span data-ttu-id="1c623-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c623-125">RELATED LINKS</span></span>
