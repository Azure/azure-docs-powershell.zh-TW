---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 6fa598b792d04d8223aafdb39405a69ada6e5915
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905582"
---
# <span data-ttu-id="afa5e-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="afa5e-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="afa5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="afa5e-102">SYNOPSIS</span></span>
<span data-ttu-id="afa5e-103">建立新實例 DataMigration Azure ActiveDirectory 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="afa5e-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="afa5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="afa5e-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afa5e-105">描述</span><span class="sxs-lookup"><span data-stu-id="afa5e-105">DESCRIPTION</span></span>
<span data-ttu-id="afa5e-106">建立新實例 DataMigration Azure ActiveDirectory 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="afa5e-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="afa5e-107">例子</span><span class="sxs-lookup"><span data-stu-id="afa5e-107">EXAMPLES</span></span>

### <span data-ttu-id="afa5e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="afa5e-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="afa5e-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey : System.Security.SecureString TenantId : "Tenant Id"</span><span class="sxs-lookup"><span data-stu-id="afa5e-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="afa5e-110">參數</span><span class="sxs-lookup"><span data-stu-id="afa5e-110">PARAMETERS</span></span>

### <span data-ttu-id="afa5e-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="afa5e-111">-AppKey</span></span>
<span data-ttu-id="afa5e-112">Azure Active Directory 金鑰</span><span class="sxs-lookup"><span data-stu-id="afa5e-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="afa5e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="afa5e-113">-ApplicationId</span></span>
<span data-ttu-id="afa5e-114">Azure Active Directory 應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="afa5e-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="afa5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa5e-115">-DefaultProfile</span></span>
<span data-ttu-id="afa5e-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="afa5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afa5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa5e-117">CommonParameters</span></span>
<span data-ttu-id="afa5e-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="afa5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="afa5e-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="afa5e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa5e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="afa5e-120">INPUTS</span></span>

### <span data-ttu-id="afa5e-121">沒有</span><span class="sxs-lookup"><span data-stu-id="afa5e-121">None</span></span>

## <span data-ttu-id="afa5e-122">輸出</span><span class="sxs-lookup"><span data-stu-id="afa5e-122">OUTPUTS</span></span>

### <span data-ttu-id="afa5e-123">Microsoft.Azure.Commands.DataMigration.models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="afa5e-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="afa5e-124">筆記</span><span class="sxs-lookup"><span data-stu-id="afa5e-124">NOTES</span></span>

## <span data-ttu-id="afa5e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="afa5e-125">RELATED LINKS</span></span>
